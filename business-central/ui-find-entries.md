---
title: Søke etter poster | Microsoft Docs
description: Denne artikkelen beskriver hvordan du finner dokumenter og poster som er relatert
author: jswymer
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: find
ms.date: 10/01/2020
ms.author: jswymer
ms.openlocfilehash: 870cd32dc2408236ed8997e1f939c00d1bf519e4
ms.sourcegitcommit: ddbb5cede750df1baba4b3eab8fbed6744b5b9d6
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 10/01/2020
ms.locfileid: "3927704"
---
# <a name="finding-related-entries-for-posted-documents"></a>Søke etter relaterte poster for bokførte dokumenter 

I denne artikkelen lærer du hvordan du finner dokumenter og poster som er knyttet til hverandre basert på en felles informasjon, for eksempel:

- Bilagsnummer eller bokføringsdato
- Forretningskontakttype, nummer eller eksternt dokumentnummer
- Vareserienummer eller partinummer

Denne funksjonen er svært nyttig for å finne postene som resulterer fra bestemte transaksjoner. Når du søker ved hjelp av bilagsnummer, kan du skrive ut oversikten fra Bilagsposter-rapporten.

## <a name="get-started"></a>Kom i gang

Funksjonen for å finne poster er lett tilgjengelig på de fleste sider som viser bokførte dokumenter eller bokførte dokumentposter, for både lister og kort. Det første trinnet er derfor å åpne én av disse sidene. Velg deretter handlingen **Søk etter poster**, eller trykk på Alt+G.

Siden **Søk etter poster** inkluderer alle relaterte dokumenter og poster basert på bilagsnr. og bokføringsdato. Siden er delt inn i tre deler:

- Den øverste delen viser felt og handlinger som du bruker til å filtrere søket.
- Den midterste delen viser relaterte dokumenter basert på søket.
- Den nederste delen viser informasjon om kildedokumentet som ble funnet ved å søke.


<!--
 There are two ways to open this page:

- Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Find Entries**, and then choose the related link.

    With this way, the **Find Entries** page might be empty, and you'll have to start searching for entries from scratch.
    
- Open a page that displays posted documents or posted documents entries, either a list or a card. Then, locate and select the **Find Entries** action.

    With this way, the **Find Entries**, page will include all related documents and entries based on the document no. and posting date.


    > [!TIP]
    > If you are on a page that has the **Find Entries** action, press crtl+G to open the **Find Entries** page directly. 
-->

## <a name="search-for-entries"></a>Søke etter poster

Du kan søke etter oppføringer basert på informasjon om enten dokumentet, forretningskontakten eller varereferansen. Du kan endre søket ved å velge **Handlinger**, **Finn etter**, og deretter én av følgende handlinger:

|Handling|Beskrivelse|
|------|-----------|
|Finn etter dokument|Vis poster basert på et bestemt bilagsnummer eller en bestemt bokføringsdato.|
|Forretningskontakt |Vis poster basert på en bestemt kontakttype, kontaktnummer og/eller eksternt dokumentnummer. Du kan skrive inn dokumentinformasjon som ble tilordnet av en leverandør eller en kunde. Bruk de tilgjengelige feltene til å søke etter leverandørs bilagsnummer ved hjelp av numrene som leverandøren har knyttet til dokumentene.|
|Varereferanse|Vis poster basert på serienummer eller partinummer. Du kan angi partinummeret eller serienummeret, eller filtrere på partinummeret eller serienummeret du vil søke etter. Denne handlingen er nyttig hvis du vil se hvor et bestemt varesporingsnummer er brukt, hvilken leverandør det kom fra, eller hvilken kunde det ble solgt til.|

Når du har gjort et valg, angir du relevant søkeinformasjon i feltene øverst. Bruk verktøytipsene i feltene som hjelp. Når du er ferdig, velger du **Søk** for å starte søket. Hvis du endrer noen av filtrene, må du velge **Søk** på nytt.

> [!TIP]
> Hvis du vil ha et par eksempler på hvordan du bruker **Søk etter poster**, kan du se [Spore varesporede varer](inventory-how-to-trace-item-tracked-items.md) og [Gjennomgang: spore serie-/partinumre](walkthrough-tracing-serial-lot-numbers.md).

## <a name="see-related-training-at-microsoft-learn"></a>Se relatert opplæring på [Microsoft Learn](/learn/modules/user-interface-dynamics-365-business-central/index)

## <a name="see-also"></a>Se også

[Arbeide med Business Central](ui-work-product.md)  
[Legge til en sidehandling i rollesenteret](ui-bookmarks.md)  
[Spore varesporede varer](inventory-how-to-trace-item-tracked-items.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]