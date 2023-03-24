---
title: Del data
description: Lær om ulike måter å dele forretningsdata på fra Business Central.
author: jswymer
ms.topic: conceptual
ms.workload: na
ms.search.keywords: null
ms.date: 09/21/2022
ms.author: jswymer
---
# Del forretningsdata fra Business Central

Samarbeid mellom personer i og utenfor en organisasjon er vesentlig del av de fleste bedrifter. [!INCLUDE[prod_short](includes/prod_short.md)] inneholder flere funksjoner for deling av forretningsdata, for eksempel lister over poster, bestemte poster eller dokumenter. <!--, with others&mdash;even those people who don't have a Business Central license in some cases.-->

Med alle disse funksjonene er tilgang til data beskyttet av lisensen og tillatelsene for Business Central.

## Kopier en kobling

![Støttes](media/check.png) Business Central Online ![Støttes](media/check.png) Business Central On-premises

Fra en hvilken som helst side kan du kopiere nettadressen til siden, lime den inn og distribuere den i andre medier som e-post, Teams-chatter eller tekstmeldinger. Den enkleste måten å kopiere en kobling på er å velge **Del** > **Kopier kobling** fra toppen av siden. En annen måte er å kopiere nettadressen direkte fra adresselinjen i nettleseren.

### Endre sidekoblingen

Når du har kopiert en kobling før du sender den, kan du endre nettadressen for å manipulere hva som vises når siden åpnes. Du kan for eksempel legge til filtre eller angi et annet selskap.

Hvis du vil ha mer informasjon, kan du se [Nettadresse for nettklient](/dynamics365/business-central/dev-itpro/developer/devenv-web-client-urls).

### Om filtrerte lister

Ved hjelp av filtreringsruten på listesider kan du bruke filtre til å begrense antallet poster som vises i listen. Hvis du bruker **Kopier kobling**-handlingen eller kopierer nettadressen fra nettleseren, vil ikke sidekoblingen inneholde filterendringene. Brukere som åpner koblingen, vil se hele samlingen. Måten du beholder filtreringen på en samlingssidekobling på, er å lagre den filtrerte siden som en **visning** først. Deretter åpner du visningen og kopierer koblingen derfra.

Hvis du vil ha mer informasjon, kan du se [Sortere, søke etter og filtrere](ui-enter-criteria-filters.md).

## Deling til Teams

![Støttes](media/check.png) Business Central Online ![Støttes ikke](media/x-icon.png) Business Central On-premises

Direkte fra de fleste samlingssider og detaljsider kan du sende en kobling til siden til personer, gruppesamtaler eller kanaler. Du kan for eksempel dele en kobling til en filtrert visning av postene. Hvis du har installert [!INCLUDE[prod_short](includes/prod_short.md)]-appen for Teams, vil koblingen automatisk utvides til et kompaktkort for at du skal kunne ta med meldingen. Mottakerne velger deretter koblingen eller kortet for å åpne siden i Business Central.

Hvis du vil ha mer informasjon, kan du se [Del oppføringer og sidekoblinger i Teams](across-working-with-teams.md).

## Deling gjennom OneDrive

![Støttes](media/check.png) Business Central Online ![Støttes](media/check.png) Business Central On-premises

Business Central gjør det enkelt å lagre, behandle og dele filer med andre personer via OneDrive for Business. På de fleste sider der filer er tilgjengelige, for eksempel rapportinnboksen eller filer som er knyttet til poster, finner du handlingene **Åpen i OneDrive** og **Del**. Begge handlingene lagrer en kopi av en fil i OneDrive. I OneDrive kan du bruke delings- og distribusjonsfunksjonene i filen. Forskjellen i handlingene er at **Åpne i OneDrive** åpner filen i OneDrive. **Del** åpner en side du kan bruke til å velge hvem du vil dele filen med. Mottakerne vil få en e-postmelding om å få tilgang til filen fra din OneDrive.

Hvis du vil ha mer informasjon, kan du se [Del filer i OneDrive](across-share-onedrive.md).

## Åpne i Excel

![Støttes](media/check.png) Business Central Online ![Støttes](media/check.png) Business Central On-premises

For listesider og lister som er innebygd på en side, kan du bruke handlingen **Åpne i Excel**. Denne handlingen eksporterer listen over poster til en Excel-arbeidsbok (XLSX-fil), som du kan dele med andre. I arbeidsboken kan du også bruke Del-funksjonen som er en del av Excel.

Hvis du vil ha mer informasjon, kan du se [Vis og rediger i Excel](across-work-with-excel.md).

## Del rader eller tabeller

![Støttes](media/check.png) Business Central Online ![Støttes](media/check.png) Business Central On-premises

Du kan dele en eller flere poster i en liste. Velg på <kbd>Ctrl</kbd>+<kbd>C</kbd>-hurtigtasten for å kopiere til utklippstavlen. Deretter limer du inn det du kopierte til et annet program ved å trykke på <kbd>Ctrl</kbd>+<kbd>V</kbd>. Hvis du for eksempel kopierer tre salgsordrer og limer inn i en e-postmelding, vises ordrene i en tabell med en pen formatering.

Hvis du vil ha mer informasjon, kan du se [Vanlige spørsmål om kopiere og lime inn](faq-copy-paste.yml).

## Se også

[Business Central og OneDrive-integrering](across-onedrive-overview.md)  
[Administrere OneDrive-integrering med Business Central](admin-onedrive-integration.md)  
[Vanlige spørsmål om OneDrive](admin-onedrive-faq.md)