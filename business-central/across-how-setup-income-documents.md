---
title: Konfigurere inngående dokumenter| Microsoft-dokumentasjon
description: Bruke funksjonen Inngående dokumenter til å opprette elektroniske dokumenter, behandle OCR-oppgaver, importere fakturaer og konvertere bildefiler.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: electronic document, e-invoice, incoming document, OCR, ecommerce, document exchange, import invoice
ms.date: 04/01/2019
ms.author: sgroespe
ms.openlocfilehash: 7e99f4b33767a1bdea7b942d1b183edbacc829ac
ms.sourcegitcommit: bd78a5d990c9e83174da1409076c22df8b35eafd
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 03/31/2019
ms.locfileid: "932744"
---
# <a name="set-up-incoming-documents"></a>Konfigurere inngående dokumenter
Hvis du oppretter finanskladdelinjer fra innkommende dokumentposter, må du angi hvilken kladdemal og kladd som skal brukes på siden **Oppsett for inngående dokumenter**.

Hvis du ikke vil at brukerne skal opprette fakturaer eller finanskladdelinjer fra innkommende dokumentposter med mindre dokumentene først er godkjent, må du definere godkjennere på siden **Godkjennere for inngående dokumenter**.

Hvis du vil gjøre om PDF- og bildefiler til elektroniske dokumenter som du kan konvertere til, for eksempel kjøpsfakturaer i [!INCLUDE[d365fin](includes/d365fin_md.md)], må du først sette opp OCR-funksjonen og aktivere tjenesten.

Når funksjonen for inngående dokumenter er konfigurert, kan du bruke forskjellige funksjoner til å se gjennom utgiftskvitteringer, behandle OCR-oppgaver og konvertere inngående dokumentfiler, manuelt eller automatisk, til de aktuelle dokumentene eller kladdelinjene. De eksterne filene kan tilknyttes på et hvilket som helst tidspunkt i prosessen, inkludert bokførte dokumenter og resulterende leverandør, kunde- og finansposter. Hvis du vil ha mer informasjon, kan du se [Behandle inngående dokumenter](across-process-income-documents.md).

## <a name="to-set-up-the-incoming-documents-feature"></a>Slik konfigurerer du funksjonen for inngående dokumenter:
1. Velg ikonet ![lyspære som åpner Fortell meg-funksjonen](media/ui-search/search_small.png "Fortell hva du vil gjøre") ikonet, angi **Oppsett for inngående dokumenter**, og velg deretter den relaterte koblingen.
2. Fyll ut feltene etter behov. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

## <a name="to-set-up-approvers-of-incoming-document-records"></a>Slik definerer du godkjennere av inngående dokumentposter:
1. Velg ikonet ![lyspære som åpner Fortell meg-funksjonen](media/ui-search/search_small.png "Fortell hva du vil gjøre") ikonet, angi **Oppsett for inngående dokumenter**, og velg deretter den relaterte koblingen.  
2. På siden **Oppsett for inngående dokumenter** velger du handlingen **Godkjennere**.

    Siden **Godkjennere for inngående dokumenter** viser alle brukerne som er definert i [!INCLUDE[d365fin](includes/d365fin_md.md)].  
3. Velg én eller flere brukere som kan godkjenne et innkommende dokument før det kan opprettes en relatert dokument- eller kladdelinje.

Når godkjennere er definert på siden **Godkjennere for inngående dokumenter**, er det bare disse brukerne som kan godkjenne et inngående dokument hvis det er merket av for **Krev godkjenning for opprettelse** på siden **Oppsett for inngående dokumenter**.

> [!NOTE]  
>   Dette godkjenningsoppsettet er ikke relatert til arbeidsflyter for godkjenning. Hvis du vil ha mer informasjon, kan du se [Bruke godkjenningsarbeidsflyter](across-how-use-approval-workflows.md).

## <a name="to-set-up-an-ocr-service"></a>Slik definerer du en OCR-tjeneste:
1. Velg ikonet ![lyspære som åpner Fortell meg-funksjonen](media/ui-search/search_small.png "Fortell hva du vil gjøre") ikonet, angi **Oppsett for OCR-tjeneste**, og velg deretter den relaterte koblingen.
2. Fyll ut feltene etter behov. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

> [!NOTE]  
> Påloggingsdataene krypteres automatisk.

## <a name="see-also"></a>Se også
[Behandle inngående dokumenter](across-process-income-documents.md)  
[Inngående dokumenter](across-income-documents.md)  
[Innkjøp](purchasing-manage-purchasing.md)  
[Arbeide med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)
