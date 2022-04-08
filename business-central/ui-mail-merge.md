---
title: Bruke Word-maler til massekommunikasjon | Microsoft-dokumentasjon
description: Word-maler kan gjøre det enkelt å opprette dokumenter som er tilpasset for bestemte enheter.
author: brentholtorf
ms.topic: get-started-article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: document, mail, merge, Word, template, email
ms.date: 04/01/2021
ms.author: bholtorf
ms.openlocfilehash: afc3391712ca33ae01d916dc4f9ed2421a0451f0
ms.sourcegitcommit: 8a12074b170a14d98ab7ffdad77d66aed64e5783
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 03/31/2022
ms.locfileid: "8519521"
---
# <a name="use-word-templates-for-bulk-communication"></a>Bruk Word-maler til massekommunikasjon
Microsoft Word-maler kan gjøre det enklere å massekommunisere på trykk eller e-post med enheter som kontakter, kunder og leverandører. Du kan for eksempel opprette brosjyrer for å varsle kunder om en salgskampanje, brev til å informere leverandører om en ny kjøpspolicy, eller invitasjoner til å tiltrekke kontakter til et kommende arrangement.

> [!NOTE]
> Du kan bare bruke Word-maler på enheter som har Microsoft Word 2019 og Windows-operativsystemet installert.

Du kan bruke enheter i [!INCLUDE[prod_short](includes/prod_short.md)] som datakilde for malen, og legge til flettefelt for å tilpasse dokumenter for hver enhet. Flettefeltene kommer fra enheten i [!INCLUDE[prod_short](includes/prod_short.md)]. Når du bruker en Word-mal på en enhet, settes det inn data fra flettefeltene i dokumentet.

På siden **Word-maler** når du oppretter en ny mal, kan du bruke en veiledning for assistert oppsett til å laste ned en ZIP-fil som inneholder filen DataSource.xlsx og en Word-malfil for enheten. Datakildefilen inneholder feltene du kan bruke i malen. Du må ikke redigere datakildefilen. Du kan bare bruke Word-maler og datakildefiler du laster ned fra [!INCLUDE[prod_short](includes/prod_short.md)], og du må lagre filene på samme sted.

Når du har definert malen og lagt til flettefelt, bruker du den samme håndboken til å laste opp malen.

## <a name="setting-up-the-template-in-word"></a>Definer malen i Word
Når du definerer en mal i Word, kan du legge til flettefelt ved å velge **Sett inn flettefelt** i fanen **Masseutsendelser**. Flettefeltene som er tilgjengelige, kommer fra datakildefilen du lastet ned for enheten. De fungerer som plassholdere som forteller Word hvor i dokumentet det skal plasseres informasjon om enheten. 

:::image type="content" source="media/word-tmpl-merge-field.PNG" alt-text="Legg til flettefelt i Microsoft Word":::

## <a name="adding-related-entities"></a>Legg til relaterte enheter
I tillegg til å legge til data for kildeenheten, det vil si enheten du oppretter malen for, kan du også slå sammen data fra enheter som er knyttet til den. Hvis for eksempel kilden er kundeenheten, kan du også slå sammen data fra felt i kunde-/innkjøperenheten, fordi begge enhetene har et felles felt.

Relaterte enheter deler et felt, som ofte er en identifikator, for eksempel navn, kode eller ID, med kildeenheten. Når du definerer en mal, er det enkle og avanserte alternativer for å velge relaterte enheter:

* Enkelt – legg til kjente relasjoner som [!INCLUDE[prod_short](includes/prod_short.md)] gjør tilgjengelige som standard.
* Avansert – legg til relasjoner som ikke er standard, for eksempel de som er lagt til av utvidelser eller tilpasninger. Dette krever at du kjenner feltene som enhetene deler.

Når du legger til en relatert enhet, må du angi et prefiks for feltnavnet. Når du legger til felt i malen, kan prefikset gjøre det enklere å skille mellom felter fra kildeenheten og feltene fra relaterte enheter.

## <a name="to-create-a-word-template-in-business-central"></a>Slik oppretter du en Word-mal i Business Central
1. Velg ikonet ![Lyspære som åpner funksjonen Fortell meg.](media/ui-search/search_small.png "Fortell hva du vil gjøre") og skriv inn **Word-maler**, og velg deretter den relaterte koblingen.
2. Velg **Ny**, **Opprett en mal**, og følg deretter instruksjonene i veiledningen for assistert oppsett. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

> [!TIP]
> Du kan også opprette en mal direkte fra siden for en enhet ved å velge handlingen **Bruk Word-mal** for å åpne veiledningen for assistert oppsett og deretter **Ny mal**. Når du gjør dette, velges datakilden basert på enhetstypen.

## <a name="applying-a-template"></a>Bruk en mal
Når Word-malen er klar, kan du velge **Bruk** på siden **Word-maler** for å generere dokumentene. Når du bruker en Word-mal på en enhet, settes det inn data fra flettefeltene i dokumentet. Du kan enten opprette ett dokument som inneholder inndelinger for hver enkelt enhet, eller velge **Del opp** for å opprette et nytt dokument for hver enhet.

Du kan bruke maler på en eller flere av den samme enhetstypen, for eksempel en kontakt, direkte i konteksten til denne siden, eller fra siden for Word-maler for å bruke malen på alle enheter av denne typen.

## <a name="use-word-templates-with-email"></a>Bruk Word-maler med e-post
Du kan bruke Word-maler til å legge til innhold i e-postmeldinger. Når du skriver en e-postmelding, kan du velge handlingen **Bruk Word-mal** for å bruke innholdet i en mal på meldingen. Dette forutsetter at du har opprettet en eller flere maler for enheten. Du kan bruke én mal om gangen, og når du bytter mellom maler, endres meldingen for å gjenspeile innholdet fra den valgte malen.

I tillegg kan du bruke handlingen **Legg til fil fra Word-mal** til å knytte innholdet i malen til e-postmeldingen som en fil. Filen bruker formatet som er angitt for utdataene i malen.

:::image type="content" source="media/email-word-tmpl.PNG" alt-text="Alternativer for bruk av innhold fra en Word-mal i en e-post":::

## <a name="see-also"></a>Se også
[Administrere rapport- og dokumentoppsett](ui-manage-report-layouts.md)  
