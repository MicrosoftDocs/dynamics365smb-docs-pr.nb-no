---
title: Business Central og OneDrive for Business-integrering
description: Du kan bruke OneDrive for Business til å lagre, behandle og dele filer, for eksempel rapporter eller filvedlegg. Også hvis du staver det One Drive.
author: jswymer
ms.topic: overview
ms.workload: na
ms.search.keywords: ''
ms.date: 02/28/2022
ms.author: jswymer
ms.openlocfilehash: 06adf2a30a7487fa3bc66e1aebec42e6c55184e2
ms.sourcegitcommit: bb9b2b4e693fa326a13d94e5e83f60e6c7ac5b68
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 08/06/2022
ms.locfileid: "9227422"
---
# <a name="business-central-and-onedrive-for-business-integration"></a>Business Central og OneDrive for Business-integrering

OneDrive for Business er en skylagringstjeneste som er inkludert i Microsoft 365. [!INCLUDE[prod_short](includes/prod_short.md)] gjør det enkelt å lagre, behandle og dele filer med andre personer via OneDrive. Når en fil befinner seg i OneDrive, kan du se de omfattende samarbeidsopplevelsene fra nettversjonene av Microsoft-produkter, for eksempel Word, Excel og PowerPoint. Du kan for eksempel dele et Word-dokument, og deretter kan du og kollegene redigere det sammen i sanntid. Med OneDrive kan du også åpne andre filtyper, for eksempel PDF-filer. 

## <a name="get-started"></a>Kom i gang

Vi har opprettet tilkoblingen mellom [!INCLUDE[prod_short](includes/prod_short.md)] online og OneDrive, slik at den er lett å komme i gang. Det eneste kravet er at brukerne har åpnet OneDrive minst én gang. 

På de fleste sider der filer er tilgjengelige, for eksempel rapportinnboksen eller filer som er knyttet til poster, finner du handlingene **Åpen i OneDrive** og **Del**.

:::image type="content" source="media/onedrive-overview-report-inbox-w-outline.png" alt-text="Handlingene Åpne i OneDrive og Del for rapporter":::


:::image type="content" source="media/one-drive-attachments-w-outline.png" alt-text="Handlingene Åpne i OneDrive og Del for vedlegg":::

|Velger du ...|Til ...|Se mer informasjon ...|
|---------|-----|----------------|
|Åpne i OneDrive|Kopier filen til en Business Central-mappe i OneDrive-filen, og åpne filen.|[Åpne i OneDrive](across-share-onedrive.md#open-in-onedrive) |
|Andel|Kopier filen til OneDrive og del den med andre personer.|[Del i OneDrive](across-share-onedrive.md#share) |

<!--
When you use the **Open in OneDrive** action for the first time, [!INCLUDE[prod_short](includes/prod_short.md)] does the following in your OneDrive:

1. Creates a folder named [!INCLUDE[prod_short](includes/prod_short.md)]. 
2. In the [!INCLUDE[prod_short](includes/prod_short.md)] folder, it creates another folder with the same name as the company you're working in. If you work in more than one company, it will create a folder for the company you're working in when you use the **Open in OneDrive** action. 
3. Puts a copy of the file you selected in the folder, and then opens the file. The next time you use the action, it only copies and opens the file. 

The folder and its content are private until you decide to share them with others. For example, you might decide to share content with one or more of your coworkers, or even people outside of your organization. For more information, see [Share OneDrive files and folders](https://support.microsoft.com/office/share-onedrive-files-and-folders-9fcc2f7d-de0c-4cec-93b0-a82024800c07) in the content for OneDrive.
-->

> [!NOTE]
> Du kan også koble [!INCLUDE[prod_short](includes/prod_short.md)] on-premises til OneDrive. Det er imidlertid et par ting du kan gjøre for å gjøre det arbeidet. Hvis du vil ha mer informasjon, kan du se [Konfigurering av Business Central On-Premises](admin-onedrive-integration.md#configuring-business-central-on-premises).

## <a name="see-also"></a>Se også

[Administrere OneDrive-integrering med Business Central](admin-onedrive-integration.md)  
[Åpne Business Central-filer i OneDrive](across-share-onedrive.md)  
[Vanlige spørsmål om OneDrive](admin-onedrive-faq.md)