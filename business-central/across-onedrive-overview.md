---
title: Business Central og OneDrive for Business-integrering
description: 'Du kan bruke OneDrive for Business til å lagre, behandle og dele filer, for eksempel rapporter eller filvedlegg. Også hvis du staver det One Drive.'
author: jswymer
ms.topic: overview
ms.search.keywords: null
ms.date: 02/28/2022
ms.author: jswymer
ms.service: dynamics-365-business-central
---

# Business Central og OneDrive for Business-integrering

OneDrive for Business er en skylagringstjeneste som er inkludert i Microsoft 365. [!INCLUDE[prod_short](includes/prod_short.md)] gjør det enkelt å lagre, behandle og dele filer med andre personer via OneDrive. Når en fil befinner seg i OneDrive, kan du se de omfattende samarbeidsopplevelsene fra nettversjonene av Microsoft-produkter, for eksempel Word, Excel og PowerPoint. Du kan for eksempel dele et Word-dokument, og deretter kan du og kollegene redigere det sammen i sanntid. Med OneDrive kan du også åpne andre filtyper, for eksempel PDF-filer. 

## Kom i gang med OneDrive-funksjoner

Hvis du bruker [!INCLUDE[prod_short](includes/prod_short.md)] online, har vi allerede opprettet tilkoblingen mellom [!INCLUDE[prod_short](includes/prod_short.md)] online og OneDrive, slik at det er lett å komme i gang. Det eneste kravet er at brukerne har åpnet OneDrive minst én gang. Med [!INCLUDE[prod_short](includes/prod_short.md)] lokal må en administrator konfigurere tilkoblingen før du kan komme i gang. Lær mer på [Administrere OneDrive-integrering med Business Central](admin-onedrive-integration.md).

<!-- We've created the connection between [!INCLUDE[prod_short](includes/prod_short.md)] online and OneDrive, so it's easy to get started. The only requirement is that users have opened OneDrive at least one time. -->

### Åpne og dele i OneDrive

På de fleste sider der filer er tilgjengelige, for eksempel rapportinnboksen eller filer som er knyttet til poster, finner du handlingene **Åpen i OneDrive** og **Del**.

:::image type="content" source="media/onedrive-overview-report-inbox-w-outline.png" alt-text="Handlingene Åpne i OneDrive og Del for rapporter":::


:::image type="content" source="media/one-drive-attachments-w-outline.png" alt-text="Handlingene Åpne i OneDrive og Del for vedlegg":::

|Velger du ...|Til ...|Se mer informasjon ...|
|---------|-----|----------------|
|Åpne i OneDrive|Kopier filen til en Business Central-mappe i OneDrive-filen, og åpne filen.|[Åpne i OneDrive](across-share-onedrive.md#open-in-onedrive) |
|Andel|Kopier filen til OneDrive og del den med andre personer.|[Del i OneDrive](across-share-onedrive.md#share) |

### Lagre Excel-arbeidsbøker og rapport filer i OneDrive

Når OneDrive-integrasjon er konfigurert, vil et par andre velkjente funksjoner automatisk bruke OneDrive til lagring av filer i stedet for å lagre filer på enheten:

- Handlingene **Åpne i Excel** og **Rediger i Excel** på listesider kopierer automatisk Excel-filen til OneDrive og åpner den deretter i Excel Online. Hvis du vil ha mer informasjon, kan du se [Vis og rediger i Excel](across-work-with-excel.md).
- Sending av en rapport til en Excel- eller Word-fil, kopieres filen automatisk til OneDrive, og deretter åpnes den i Excel eller Word på nettet. Hvis du vil ha mer informasjon, kan du se [Lagre en rapport til en fil](ui-work-report.md#saving-a-report-to-a-file).

Disse funksjonene er ikke aktivert som standard. Men som administrator kan du enkelt aktivere dem ved hjelp av assistert oppsettsveiledning for **OneDrive-oppsett**.

<!--
When you use the **Open in OneDrive** action for the first time, [!INCLUDE[prod_short](includes/prod_short.md)] does the following in your OneDrive:

1. Creates a folder named [!INCLUDE[prod_short](includes/prod_short.md)]. 
2. In the [!INCLUDE[prod_short](includes/prod_short.md)] folder, it creates another folder with the same name as the company you're working in. If you work in more than one company, it will create a folder for the company you're working in when you use the **Open in OneDrive** action. 
3. Puts a copy of the file you selected in the folder, and then opens the file. The next time you use the action, it only copies and opens the file. 

The folder and its content are private until you decide to share them with others. For example, you might decide to share content with one or more of your coworkers, or even people outside of your organization. For more information, see [Share OneDrive files and folders](https://support.microsoft.com/office/share-onedrive-files-and-folders-9fcc2f7d-de0c-4cec-93b0-a82024800c07) in the content for OneDrive.
-->

> [!NOTE]
> Du kan også koble [!INCLUDE[prod_short](includes/prod_short.md)] on-premises til OneDrive. Det er imidlertid et par ting du kan gjøre for å gjøre det arbeidet. Hvis du vil ha mer informasjon, kan du se [Konfigurering av Business Central On-Premises](admin-onedrive-integration-onpremises.md).

## Se også

[Administrere OneDrive-integrering med Business Central](admin-onedrive-integration.md)  
[Åpne Business Central-filer i OneDrive](across-share-onedrive.md)  
[Vanlige spørsmål om OneDrive](admin-onedrive-faq.md)  
