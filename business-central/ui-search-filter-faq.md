---
title: Om søking og filtrering i Business Central
description: Svar på vanlige spørsmål om søking og filtrering.
author: mikebcMSFT
ms.service: dynamics365-business-central
ms.topic: article
ms.reviewer: edupont04
ms.search.keywords: keyboarding, productivity, how do i, filter pane
ms.date: 10/01/2019
ms.author: mikebc
ms.openlocfilehash: 93a68509653aef29bb8f798e7fded70bab550e13
ms.sourcegitcommit: 02e704bc3e01d62072144919774f1244c42827e4
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 10/01/2019
ms.locfileid: "2315063"
---
# <a name="searching-and-filtering-faq"></a>Vanlige spørsmål om søk og filtrering
Denne artikkelen svarer på vanlige spørsmål du måtte ha om søking og filtrering.

## <a name="is-there-a-difference-between-searching-and-filtering"></a>Er det forskjell mellom søking og filtrering?
Ja.
- Søking er enkelt og bredt: Det samsvarer poster som inneholder tekst på tvers av alle feltene som vises på siden, og er skiller ikke mellom store/små bokstaver.
- Filtrering er svært fleksibelt og kan brukes mot et bestemt felt, inkludert de som ikke vises på siden: Det viser poster med nøyaktige treff som skiller mellom store/små bokstaver, men kan endres med effektive søkesymboler, spesialtegn og formler. Hvis du vil ha mer informasjon om hvordan du bruker disse funksjonene, se [Sortere, søke etter og filtrere](ui-enter-criteria-filters.md).

## <a name="is-there-a-keyboard-experience-for-search-and-filter"></a>Er det en tastaturopplevelse for søking og filtrering?
Søking og filtrering har blitt svært optimalisert for brukere som foretrekker musfri samhandling for å arbeide effektivt med data. Det finnes en rekke hurtigtaster som kan brukes i rekkefølge til å arbeide raskt. Hvis du vil ha mer informasjon, kan du se [Hurtigtaster](keyboard-shortcuts.md#KeyboardFilter)

## <a name="is-the-filter-pane-available-on-all-lists"></a>Er filtreringsruten tilgjengelig i alle lister?
Filtreringsruten er tilgjengelig på sidene der listen er det primære innholdet på siden, for eksempel forslag og listesider, inkludert lister som er tilgjengelig fra navigasjonslinjen. Filtreringsruten er ennå ikke tilgjengelig for lister som vises som deler, for eksempel faktabokser eller rollesenterdeler. Når en liste er innebygd på en side, for eksempel salgslinjer i en ordre, er filtreringsruten tilgjengelig når du fokuserer på denne listen ved hjelp av fokusmodusknappen. Hvis du vil ha mer informasjon, se [Fokusere på linjeelementer](ui-enter-data.md#Focus).

## <a name="how-can-i-save-my-filters"></a>Hvordan lagrer jeg filtre?
Filtrene og justeringene dine i forhåndsdefinerte filtre huskes gjennom økten (mens du er logget på), selv om du navigerer bort fra siden. Du kan lagre filtre permanent som en navngitt visning av listen ved å velge ikonet ![Lagre visning](media/save_view_icon.png "Lagre visning") i filtreringsruten. Hvis du vil ha mer informasjon, kan du se [Vanlige spørsmål om listevisninger](ui-views-faq.md). I motsetning til filtre blir ikke søketeksten husket når du navigerer bort fra en side, og lagres ikke når du lagrer en visning.

På rapportforespørselssider kan du også lagre filtre eller bruke forhåndsdefinerte filtre. Hvis du vil ha mer informasjon, kan du se [Bruke lagrede innstillinger](ui-work-report.md#SavedSettings).

## <a name="is-this-the-same-as-advanced-filters-and-limit-totals-in-microsoft-dynamics-nav"></a>Er dette det samme som Avanserte filtre og Begrens totaler i Microsoft Dynamics NAV?
[!INCLUDE[d365fin](includes/d365fin_md.md)] bygger på disse populære funksjonene og gir deg en moderne og brukervennlig opplevelse for å finne og analysere data. Med flere hurtigtaster og innføringen av Søk overgår [!INCLUDE[d365fin](includes/d365fin_md.md)] funksjonaliteten i Dynamics NAV.  

## <a name="can-i-search-and-filter-using-the-companion-apps-and-outlook-addin"></a>Kan jeg søke og filtrere ved hjelp av medfølgende apper og Outlook-tillegget?
På andre visningsmål, for eksempel mobilenheter eller Outlook, kan du søke i lister, men ikke filtrere på enkeltfelt i de fleste tilfeller.

## <a name="will-microsoft-extend-the-filter-pane-experience"></a>Vil Microsoft utvide filtreringsruteopplevelsen?
Hos Microsoft hører vi konstant på tilbakemelding fra våre mange brukere og agerer på de mest populære forslagene. Hvis du er interessert i å utvide filtreringsturen til flere formfaktorer og flere typer oversikter eller har en god idé om hvordan du kan forbedre den, kan du legge til en idé eller stemme på eksisterende idéer på [aka.ms/BusinessCentralIdeas](https://aka.ms/businesscentralideas).

## <a name="can-i-do-anything-about-the-searching-for-rows-is-taking-too-long-message"></a>Kan jeg gjore noe med meldingen "Søk etter rader tar for lang tid"?

Det er en tidsbegrensning på hvor lenge en søkeoperasjon kan ta. Prøv først å endre søkekriteriene og søk på nytt. Hvis du bruker [!INCLUDE[prodshort](includes/prodshort.md)] lokalt, kontakt systemadministratoren, fordi en administrator kan øke tidsfristen for søk.

Som en lokal administrator kan du øke tidsgrensen for søk ved å endre innstillingen **Tidsavbrudd for søk** for [!INCLUDE[prodshort](includes/prodshort.md)]-serveren. Hvis du vil ha mer informasjon, se [Konfigurere Business Central Server](https://docs.microsoft.com/en-us/dynamics365/business-central/dev-itpro/administration/configure-server-instance?#Database) i hjelpen for utviklere og IT-eksperter for Business Central.

## <a name="see-also"></a>Se også
[Sortere, søke etter og filtrere](ui-enter-criteria-filters.md)  
[Finne sider og informasjon med Fortell meg](ui-search.md)  
[Finne sider fra en funksjonsoversikt](ui-role-explorer.md)  
[Komme i gang](product-get-started.md)  
