---
title: Bruke Word-maler til massekommunikasjon | Microsoft-dokumentasjon
description: Word-maler kan gjøre det enkelt å opprette dokumenter som er tilpasset for bestemte enheter.
author: bholtorf
ms.service: dynamics365-business-central
ms.topic: get-started-article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: document, mail, merge, Word, template, email
ms.date: 04/01/2021
ms.author: bholtorf
ms.openlocfilehash: 84b6a9fa74cea99f8b939edcf0cd883e39eb6937
ms.sourcegitcommit: a7cb0be8eae6ece95f5259d7de7a48b385c9cfeb
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 07/08/2021
ms.locfileid: "6445975"
---
# <a name="using-word-templates-for-bulk-communication"></a>Bruke Word-maler til massekommunikasjon
Microsoft Word-maler kan gjøre det enklere å massekommunisere med enheter som kunder og leverandører. Du kan for eksempel opprette brosjyrer for å varsle kunder om en salgskampanje, brev til å informere leverandører om en ny kjøpspolicy, eller invitasjoner til å tiltrekke kontakter til et kommende arrangement.

> [!NOTE]
> Du kan bare bruke Word-maler på enheter som har Microsoft Word 2019 og Windows-operativsystemet installert.

Du kan bruke enheter i [!INCLUDE[prod_short](includes/prod_short.md)] som datakilde for malen, og legge til flettefelt for å tilpasse dokumenter for hver enhet. Flettefeltene kommer fra enheten i [!INCLUDE[prod_short](includes/prod_short.md)]. Når du bruker en Word-mal på en enhet, settes det inn data fra flettefeltene i dokumentet.

På siden **Word-maler** kan du bruke en veiledning for assistert installasjon for å laste ned en ZIP-fil som inneholder filen DataSource.txt og en Word-malfil for en enhet. Når du har definert malen og lagt til flettefelt, bruker du den samme håndboken til å laste opp malen. Du kan bare bruke Word-maler og datakildefiler du laster ned fra [!INCLUDE[prod_short](includes/prod_short.md)], og du må lagre filene på samme sted.

> [!NOTE]
> Når du velger en enhet du vil opprette en mal for, viser listen alle enhetene i [!INCLUDE[prod_short](includes/prod_short.md)]. Du kan imidlertid ikke opprette maler for alle enheter. Hvis navnet på en enhet inneholder spesialtegn, for eksempel **/**, **.**, **_** eller **-**, kan du ikke opprette en mal for den. Navnet på enheten vises i kolonnen **Objekttittel**.

Når du definerer malen i Word, kan du legge til flettefelt ved å velge **Sett inn flettefelt** i fanen **Masseutsendelser**.

> [!NOTE]
> Du kan ikke bruke flettefelt hvis navnet på feltet inneholder 40 tegn eller mer. Du kan for eksempel ikke feltet bruke Company__Information_Customs_Permit_Date, fordi det har 40 tegn. 

Når Word-malen er klar, kan du velge **Bruk** på siden **Word-maler** for å generere dokumentene. Du kan enten opprette ett dokument som inneholder inndelinger for hver enkelt enhet, eller dele opp operasjonen for å opprette et nytt dokument for hver enhet.

## <a name="to-create-a-word-template"></a>Slik oppretter du en Word-mal
1. Velg ikonet ![Lyspære som åpner funksjonen Fortell meg.](media/ui-search/search_small.png "Fortell hva du vil gjøre") og skriv inn **Word-maler**, og velg deretter den relaterte koblingen.
2. Følg trinnene i den assisterte oppsettsveiledningen. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

## <a name="see-also"></a>Se også
[Administrere rapport- og dokumentoppsett](ui-manage-report-layouts.md)  
