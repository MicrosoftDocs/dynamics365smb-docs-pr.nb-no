---
title: Hjelpefunksjoner
description: Hurtigtaster og andre hjelpefunksjoner.
author: jswymer
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: accessibility, shortcuts, charts, tooltips, screen reader
ms.date: 04/29/2021
ms.author: jswymer
ms.openlocfilehash: 5a9b99b367ca732f5b6347462a07b0d0c3f5c522
ms.sourcegitcommit: f9a190933eadf4608f591e2f1b04c69f1e5c0dc7
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 05/28/2021
ms.locfileid: "6115893"
---
# <a name="accessibility-and-keyboard-shortcuts"></a>Tilgjengelighet og hurtigtaster

Denne artikkelen inneholder informasjon om funksjonene som gjør [!INCLUDE[prod_short](includes/prod_short.md)] lett tilgjengelig for personer med funksjonshemninger. [!INCLUDE[prod_short](includes/prod_short.md)] støtter følgende tilgjengelighetsfunksjoner:  

- Hurtigtaster. Se [Hurtigtaster](keyboard-shortcuts.md).
- Berørings- og pennebevegelser på nettbrett og telefoner. Se [Berørings- og pennebevegelser](touch-gestures.md).
- Navigasjon  
- Overskrifter  
- Alternativ tekst for bilder og koblinger  
- Støtte for vanlige tekniske hjelpefunksjoner 
- Zoome inn eller ut på en side
- Verktøytips for elementer i brukergrensesnittet

## <a name="navigation"></a><a name="Navigation"></a> Navigasjon
  
Du kan bruke forskjellige kombinasjoner av TAB, SKIFT og piltastene på tastaturet til å gå mellom elementer på en side. Elementer omfatter handlinger, felt og kolonner, deler og andre kontroller. Vanligvis trykker du på TAB eller SKIFT+TAB for å gå til neste eller forrige element.

Når du fokuserer på et område som inneholder handlinger, for eksempel navigasjonsfeltet øverst i rollesenteret eller handlingsfeltet på andre sider, bruker du piltastene til å gå til de ulike handlingene og gruppene. Trykk på ENTER i en gruppe for å åpne de underliggende handlingene, og fortsett deretter å bruke piltastene. Trykk TAB eller SKIFT+TAB for å forlate handlingsområdet.

Du kan for eksempel også bruke tabulatorrekkefølgen til å bytte mellom hovedsiden i nettleseren og dialogbokser som ber om bekreftelse, eller påloggingssiden.  

## <a name="headings-in-content"></a><a name="Headings"></a> Overskrifter i innhold

HTML-kilden for [!INCLUDE[prod_short](includes/prod_short.md)]-innhold bruker koder for å hjelpe brukere av hjelpeteknologi til å forstå strukturen og innholdet på siden. For eksempel på listesider defineres kolonnene i TH-koder og kolonneoverskriftene defineres med TITTEL-attributtet inni koden. Overskrifter for elementer, for eksempel hurtigfaner faktabokser og felt, inkluderes i overskriftskoder (H1, H2, H3 og H4).  

## <a name="image-and-links"></a><a name="Images"></a> Bilde og koblinger

Det angis en beskrivende tekst for bilder med ALT-attributtet inni IMG-koden. Det angis en beskrivende tekst for hyperkoblinger med tittelattributtet inni A-koden.  

## <a name="assistive-technologies"></a><a name="AssistiveTech"></a> Hjelpeteknologi

[!INCLUDE[prod_short](includes/prod_short.md)] støtter ulike hjelpteknologier, for eksempel høy kontrast, skjermlesere og talegjenkjenningsprogramvare. Det kan være at noen hjelpeteknologier ikke fungerer godt med bestemte elementer på [!INCLUDE[prod_short](includes/prod_short.md)]-sider.  

## <a name="zoom"></a><a name="zoom"></a> Zoom

De fleste nettlesere bruker standard tastatursnarveier for å zoome inn og ut på gjeldende side. Disse hurtigtastene er ikke spesifikke for [!INCLUDE [prod_short](includes/prod_short.md)], men de fungerer når du bruker [!INCLUDE [prod_short](includes/prod_short.md)] i en nettleser. Hvis du vil se en liste over støttede hurtigtaster, kan du se [Hurtigtaster for å zoome inn og ut](keyboard-shortcuts.md#zoomshortcuts).

## <a name="tooltips"></a>Verktøytips

Verktøytips er tilgjengelige for de fleste elementene i brukergrensesnittet, for eksempel sidefelter og -kolonner, handlinger, bunkefliser og diagrammer. Et verktøytips inneholder ekstra tekst som forklarer hva som er hensikten med et element. 

Du kan vise verktøytips på ulike måter, avhengig av klienten (nett eller mobil) og enheten du arbeider med. Bruk tabellen nedenfor som en veiledning. Enkelte verktøytips kan leses av skjermlesere. I dette tilfellet får du tilgang til verktøytipsene som beskrevet i tabellen, og deretter bruker du skjermleseren til å gå til verktøytipset på samme måte som med andre elementer.

#### <a name="accessing-tooltips"></a>Få tilgang til verktøytips

|Element|Musehandling for nettklient|Hurtigtast for nettklient|Berøringsbevegelse på nettbrett/telefon for mobilapp|Støtte for skjermleser|
|-------|-----------------|------------|--------------------------|---------------------|
|Sidefelter og kolonneoverskrifter|Hold pekeren over eller klikk på feltteksten eller kolonneoverskriften|Flytt fokus til feltet eller kolonneoverskriften, og trykk på ALT+PIL OPP|Trykk på feltteksten |ja|
|Diagramelementer, for eksempel stolpe, linje, sektor|Hold pekeren over elementet|Flytt fokus til elementet, for eksempel ved å bruke piltastene|Trykk på og hold elementet|ja|
|Handlinger|Hold pekeren over handlingen|ingen|ingen |nei|
|Bunkefliser|Hold pekeren over flisen |ingen|ingen|nei|


<!--
- With a mouse, hover over the element.
- With keyboard, press the Alt+Up Arrow keys.
- On a tablet or phone, tap and hold on the element. To learn about more gestures, see [Touch and Pen Gestures](touch-gestures.md)

-->

## <a name="for-more-accessibility-information"></a>For mer informasjon om tilgjengelighet

Du finner mer informasjon om tilgjengelighet med Microsoft-produkter og hjelpeteknologi på nettstedet for [Microsoft Accessibility](https://go.microsoft.com/fwlink/?LinkId=262160).

## <a name="see-also"></a>Se også

[Bli klar til å gjøre forretninger](ui-get-ready-business.md)  
[Arbeide med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  
[Vanlige spørsmål](across-faq.yml)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
