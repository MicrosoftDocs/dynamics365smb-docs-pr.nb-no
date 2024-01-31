---
title: Feilsøk Copilot- og KI-funksjoner
description: Lær hvordan du løser vanlige problemer du kan støte på mens du arbeider med Copilot- og KI-funksjoner i Business Central.
author: jswymer
ms.author: jswymer
ms.reviewer: jswymer
ms.topic: troubleshooting
ms.collection:
  - bap-ai-copilot
ms.date: 11/15/2023
ms.custom: bap-template
---
# Feilsøk Copilot- og KI-funksjoner

Copilot er en KI-drevet funksjonalitet i Business Central som hjelper deg med ulike oppgaver som å utarbeide markedsføringstekst og avstemme bankkontoer. Hvis du opplever problemer med Copilot eller andre KI-funksjoner, kan denne artikkelen hjelpe deg med å identifisere og fikse vanlige problemer.

## Copilot vises ikke på sidene

Hvis Copilot-funksjonalitet, for eksempel **Lag utkast med Copilot**-handlingen for markedsføringstekstforslag eller **Avstem med Copilot**-handlingen for hjelp med bankkontoavstemming, vises ikke på en side som forventet, må du sjekke følgende:

- Hvis funksjonen kontrolleres under Funksjonsstyring, må du kontrollere at den er aktivert. [Finn ut mer om funksjonsstyring](admin-feature-management.md).

- Pass på at funksjonaliteten ikke er skjult av tilpassing. [Finn ut mer om tilpassing](ui-personalization-user.md).

## Copilot vises på sidene, men du får en feilmelding om at den ikke er aktivert

Når du prøver å bruke Copilot og du får en feilmelding som ligner **Beklager, men Copilot er ikke aktivert for \[funksjonen\]**, er det et par ting du kan sjekke :

- Kontroller først at funksjonen er aktivert på siden **Copilot og KI-funksjoner**. [Finn ut mer om aktivering av Copilot- og KI-funksjoner](enable-ai.md#activate-features). 
- Deretter må du sørge for at personvernerklæringen for Azure OpenAI-integrering ikke er satt til **Ikke godta for alle**. Hvis det er det, endrer du det til **Godta for alle**. [Finn ut mer om personvernerklæringer](privacy-notices-status.md).

## Se også

[Konfigurer Copilot- og KI-funksjoner](enable-ai.md)  
[Markedsføringstekstforslag med Copilot](ai-overview.md)  
[Avstemme bankkontoer med Copilot](bank-reconciliation-with-copilot.md)  
