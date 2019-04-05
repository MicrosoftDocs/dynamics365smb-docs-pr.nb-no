---
title: Om søking og filtrering i Business Central
description: Svar på vanlige spørsmål om søking og filtrering.
author: mikebcMSFT
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: keyboarding, productivity, how do i, filter pane
ms.date: 10/01/2018
ms.author: mikebc
ms.openlocfilehash: a4bcdca8ecff80d8d47bf9c198cd69a71f09cd2a
ms.sourcegitcommit: d09f5ee0e164c7716f4ccb2ed71e2f9732a1f4f9
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 03/19/2019
ms.locfileid: "852059"
---
# <a name="searching-and-filtering-faq"></a>Vanlige spørsmål om søk og filtrering
Denne artikkelen svarer på vanlige spørsmål du måtte ha om søking og filtrering.

## <a name="is-there-a-difference-between-searching-and-filtering"></a>Er det forskjell mellom søking og filtrering?
Ja.
- Søking er enkelt og bredt: Det samsvarer poster som inneholder tekst på tvers av alle feltene som vises på siden, og er skiller ikke mellom store/små bokstaver.
- Filtrering er svært fleksibelt og kan brukes mot et bestemt felt, inkludert de som ikke vises på siden: Det viser poster med nøyaktige treff som skiller mellom store/små bokstaver, men kan endres med effektive søkesymboler, spesialtegn og formler. Hvis du vil ha mer informasjon om hvordan du bruker disse funksjonene, se [Sortere, søke etter og filtrere i oversikter](ui-enter-criteria-filters.md).

## <a name="is-there-a-keyboard-experience-for-search-and-filter"></a>Er det en tastaturopplevelse for søking og filtrering?
Søking og filtrering har blitt svært optimalisert for brukere som foretrekker musfri samhandling for å arbeide effektivt med data. Det finnes en rekke hurtigtaster som kan brukes i rekkefølge til å arbeide raskt. Hvis du vil ha mer informasjon, kan du se [Hurtigtaster](keyboard-shortcuts.md#KeyboardFilter)

## <a name="is-the-filter-pane-available-on-all-lists"></a>Er filtreringsruten tilgjengelig i alle lister?
Filtreringsruten er tilgjengelig på sidene der listen er det primære innholdet på siden, for eksempel forslag og listesider, inkludert lister som er tilgjengelig fra navigasjonslinjen. Filtreringsruten er foreløpig ikke blitt tilgjengelig for innebygde lister, for eksempel salgslinjer i salgsordrer, eller for lister med dynamisk kolonner (ofte referert til som matrisesider).

## <a name="how-can-i-save-my-filters"></a>Hvordan lagrer jeg filtre?

Filtrene og justeringene dine i forhåndsdefinerte filtre huskes gjennom økten (mens du er logget på), selv om du navigerer bort fra siden. Det er for øyeblikket ikke mulig å lagre filtre permanent. I motsetning til filtre huskes ikke søketekst når du navigerer bort fra en side.

## <a name="is-this-the-same-as-advanced-filters-and-limit-totals-in-microsoft-dynamics-nav"></a>Er dette det samme som Avanserte filtre og Begrens totaler i Microsoft Dynamics NAV?
[!INCLUDE[d365fin](includes/d365fin_md.md)] bygger på disse populære funksjonene og gir deg en moderne og brukervennlig opplevelse for å finne og analysere data. Med flere hurtigtaster og innføringen av Søk overgår [!INCLUDE[d365fin](includes/d365fin_md.md)] funksjonaliteten i Dynamics NAV.

## <a name="can-i-search-and-filter-using-the-companion-apps-and-outlook-addin"></a>Kan jeg søke og filtrere ved hjelp av medfølgende apper og Outlook-tillegget?
På andre visningsmål, for eksempel mobilenheter eller Outlook, kan du søke i lister, men ikke filtrere på enkeltfelt i de fleste tilfeller.

## <a name="is-the-filter-pane-available-for-filtering-reports"></a>Er filtreringsruten tilgjengelig for filtrering av rapporter?
Nei. Dialogboksen for rapportfilter, ofte referert til som forespørselssiden, bruker en annen brukeropplevelse som inneholder noen av, men ikke alle, funksjonene i filtreringsruten.

## <a name="will-microsoft-extend-the-filter-pane-experience"></a>Vil Microsoft utvide filtreringsruteopplevelsen?
Hos Microsoft hører vi konstant på tilbakemelding fra våre mange brukere og agerer på de mest populære forslagene. Hvis du er interessert i å utvide filtreringsturen til flere formfaktorer, flere typer oversikter og rapporter eller har en god idé om hvordan du kan forbedre den, kan du legge til en idé eller stemme på eksisterende idéer på [aka.ms/BusinessCentralIdeas](https://aka.ms/businesscentralideas).

## <a name="can-i-do-anything-about-the-searching-for-rows-is-taking-too-long-message"></a>Kan jeg gjore noe med meldingen "Søk etter rader tar for lang tid"?

Det er en tidsbegrensning på hvor lenge en søkeoperasjon kan ta. Prøv først å endre søkekriteriene og søk på nytt. Hvis du bruker [!INCLUDE[prodshort](includes/prodshort.md)] lokalt, kontakt systemadministratoren, fordi en administrator kan øke tidsfristen for søk.

Som en lokal administrator kan du øke tidsgrensen for søk ved å endre innstillingen **Tidsavbrudd for søk** for [!INCLUDE[prodshort](includes/prodshort.md)]-serveren. Hvis du vil ha mer informasjon, se [Konfigurere Business Central Server](https://docs.microsoft.com/en-us/dynamics365/business-central/dev-itpro/administration/configure-server-instance?#Database) i hjelpen for utviklere og IT-eksperter for Business Central.

## <a name="see-also"></a>Se også
[Komme i gang](product-get-started.md)  
[Sortere, søke etter og filtrere i oversikter](ui-enter-criteria-filters.md)
