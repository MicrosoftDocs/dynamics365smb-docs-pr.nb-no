---
title: Åpne Business Central-filer i OneDrive
description: Finn ut hvordan du kan dele Business Central-data via OneDrive for Business.
author: jswymer
ms.topic: conceptual
ms.workload: na
ms.search.keywords: ''
ms.date: 02/28/2022
ms.author: jswymer
ms.openlocfilehash: 2e1cc04d265541c87244dcd6c13b14327f07cc2f
ms.sourcegitcommit: 8a12074b170a14d98ab7ffdad77d66aed64e5783
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 03/31/2022
ms.locfileid: "8516424"
---
# <a name="opening-and-sharing-business-central-files-in-onedrive"></a>Åpne og del Business Central-filer i OneDrive

[!INCLUDE[prod_short](includes/prod_short.md)] gjør det enkelt å lagre, behandle og dele filer med andre personer via OneDrive for Business. På de fleste sider der filer er tilgjengelige, for eksempel rapportinnboksen eller filer som er knyttet til poster, finner du handlingene **Åpen i OneDrive** og **Del**.


:::image type="content" source="media/onedrive-overview-report-inbox-w-outline.png" alt-text="Handlingene Åpne i OneDrive og Del for rapporter":::


:::image type="content" source="media/one-drive-attachments-w-outline.png" alt-text="Handlingene Åpne i OneDrive og Del for vedlegg":::

<!--
:::image type="content" source="media/Open in OneDrive.PNG" alt-text="The Open in OneDrive action":::

 
:::image type="content" source="media/OneDrive attachment.PNG" alt-text="Share file attachments in OneDrive":::
-->

## <a name="open-in-onedrive"></a>Åpne i OneDrive

Handlingen **Åpne i OneDrive** kopierer filen til OneDrive og åpner filen i de nettbaserte appene, som Excel online, Word online og PowerPoint online. 

<!--## Working with Different Types of Files-->

Når du velger **Åpne i OneDrive**, identifiserer [!INCLUDE[prod_short](includes/prod_short.md)] Excel-, Word- og PowerPoint-filer og åpner dem i nettprogrammene, det vil si Excel online, Word online og PowerPoint online. Du kan sette inn merknader, redigere og samarbeide med andre uten å forlate nettleseren.

For andre populære filtyper, for eksempel PDF-filer, tekstfiler og bilder inneholder OneDrive filvisningsprogrammer som tilbyr funksjoner for utskrift, deling og mer. Hvis en fil ikke kan vises i OneDrive, kan det hende du blir bedt om å laste den ned.

## <a name="share"></a>Andel

Handlingen **Del** kopierer filen til OneDrive og lar deg dele filen med andre personer og se hvem du allerede har delt filen med. Når du velger **Del**-handlingen, åpnes neste side.

:::image type="content" source="media/share-to-onedrive-dialog.PNG" alt-text="Del fil i OneDrive":::

Hvis du er vant med OneDrive, kan du gjenkjenne siden. Du har to alternativer for deling av filen: **Send kobling** og **Kopier kobling**.

- **Send kobling** lar deg dele filene med bestemte personer. Personene du deler filen med, får en e-postmelding med en kobling til filen. Filen vil også vises i delen **Delt** i OneDrive. Begynn med å skrive inn e-postadresser eller kontaktnavn i feltet **Navn, gruppe eller e-post**.

- **Kopier kobling** kopierer en kobling til filen i OneDrive slik at du kan bruke koblingen andre steder som Facebook, Twitter eller e-postmeldinger. 

Før du sender eller kopierer koblingen, må du angi tillatelsen for filen du vil brukere skal ha. Du kan se nåværende innstilling under **Send kobling** og **Kopier kobling**. I de fleste tilfeller vil det være **Alle med koblingen kan redigere for å åpne koblingen**, avhengig av innstillingene som er angitt av administratoren. Hvis du vil endre tillatelsene, merker du koblingen og gjør endringer på siden **Koblingsinnstillinger**.

Delingsfunksjonen i Business Central er basert på OneDrive. Hvis du vil lære mer om deling og tillatelser, kan du se [Del OneDrive-filer og -mapper](https://support.microsoft.com/en-us/office/share-onedrive-files-and-folders-9fcc2f7d-de0c-4cec-93b0-a82024800c07).

> [!NOTE]
> Handlingen **Del** er ikke tilgjengelig i Business Central-appen for mobilenheter.

## <a name="first-time-sign-in-from-business-central"></a>Førstegangs pålogging fra Business Central

Når du bruker handlingen **Åpne i OneDrive** eller **Del** for første gang, gjør [!INCLUDE[prod_short](includes/prod_short.md)] følgende:

1. Åpner siden **Se gjennom vilkårene**. Les siden, og velg deretter **Godta** for å fortsette hvis du godtar vilkårene.
2. Åpner siden **Velg en konto** Velg kontoen din eller **bruk en annen konto** hvis du ikke finner din egen, og skriv inn brukernavnet og passordet når du blir bedt om det.
3. Oppretter en mappe med navnet [!INCLUDE[prod_short](includes/prod_short.md)] i OneDrive. 
4. I [!INCLUDE[prod_short](includes/prod_short.md)]-mappen opprettes det en annen mappe med samme navn som selskapet du arbeider i. Hvis du arbeider i flere enn ett selskap, opprettes det en mappe for selskapet du arbeider med, når du bruker handlingen **Åpne i OneDrive** og **Del**. 
5. Lagrer en kopi av filen du valgte i mappen, og åpner deretter filen. Neste gang du bruker handlingen, kopieres og åpnes bare filen. 

## <a name="managing-multiple-copies-of-a-file"></a>Behandle flere kopier av en fil

Når du velger **Åpne i OneDrive** eller **Del**, kopieres filen fra [!INCLUDE[prod_short](includes/prod_short.md)] til mappen i OneDrive. Hvis du redigerer filen i OneDrive, vil kopiene av filen være forskjellig. Hvis du vil oppdatere [!INCLUDE[prod_short](includes/prod_short.md)] med den siste filen, fjerner du den eksisterende filen fra [!INCLUDE[prod_short](includes/prod_short.md)], og deretter laster du opp den siste kopien.

Når en fil med samme navn allerede finnes i OneDrive, får du i tillegg et valg i [!INCLUDE[prod_short](includes/prod_short.md)] om å erstatte filen eller beholde begge filene. Hvis du velger å beholde begge filene, kopieres den nye filen til OneDrive og får et filnavn med suffiksnummer, for eksempel Varer (2). xlsx,. Den opprinnelige filen endres ikke. 

Hvis du velger å erstatte filen, legges den nye filen til i versjonsloggen for denne filen. Den opprinnelige filen går ikke tapt, og du kan vise eller gjenopprette tidligere versjoner av filen. 

## <a name="about-your-business-central-folder-on-onedrive"></a>Om Business Central-mappen på OneDrive

Mappen og innholdet er private helt til du bestemmer deg for å dele det med andre. Du kan for eksempel velge å dele innhold med en eller flere av kollegene dine, eller til og med personer utenfor organisasjonen. Du får tilgang til OneDrive fra **Mine innstillinger**-siden ved å velge koblingen i **Skylagring**-feltet. Hvis du vil ha mer informasjon, kan du se [Del OneDrive-filer og -mapper](https://support.microsoft.com/en-us/office/share-onedrive-files-and-folders-9fcc2f7d-de0c-4cec-93b0-a82024800c07).

:::image type="content" source="media/my-settings-cloud-storage.PNG" alt-text="Skylagring-feltet i Mine innstillinger":::

<!--## Extending the Connection to OneDrive
You can create an extension and connect it to... For more information, see...-->

## <a name="see-also"></a>Se også
[Business Central og OneDrive-integrering](across-onedrive-overview.md)  
[Administrere OneDrive-integrering med Business Central](admin-onedrive-integration.md)  
[Vanlige spørsmål om OneDrive](admin-onedrive-faq.md)