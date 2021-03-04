---
title: Konfigurere inngående dokumenter| Microsoft-dokumentasjon
description: Bruke funksjonen Inngående dokumenter til å opprette elektroniske dokumenter, behandle OCR-oppgaver, importere fakturaer og konvertere bildefiler.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: electronic document, e-invoice, incoming document, OCR, ecommerce, document exchange, import invoice
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: 3a43c32d90a7c27af56ed55a4625b3dc3faf498b
ms.sourcegitcommit: 2e7307fbe1eb3b34d0ad9356226a19409054a402
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 12/17/2020
ms.locfileid: "4754895"
---
# <a name="set-up-incoming-documents"></a>Konfigurere inngående dokumenter

Hvis du oppretter finanskladdelinjer fra innkommende dokumentposter, må du angi hvilken kladdemal og kladd som skal brukes på siden **Oppsett for inngående dokumenter**.

Hvis du ikke vil at brukerne skal opprette fakturaer eller finanskladdelinjer fra innkommende dokumentposter med mindre dokumentene først er godkjent, må du definere arbeidsflytgodkjennere.

Hvis du vil gjøre om PDF- og bildefiler til elektroniske dokumenter som du kan konvertere til, for eksempel kjøpsfakturaer i [!INCLUDE[prod_short](includes/prod_short.md)], må du først sette opp OCR-funksjonen og aktivere tjenesten. Velg en tjenestepakke som passer for organisasjonen og/eller landet/området. Du kan også opprette poster manuelt for å representere de eksterne dokumentene.  

Når funksjonen for inngående dokumenter er konfigurert, kan du bruke forskjellige funksjoner til å se gjennom utgiftskvitteringer, behandle OCR-oppgaver og konvertere inngående dokumentfiler, manuelt eller automatisk, til de aktuelle dokumentene eller kladdelinjene. De eksterne filene kan tilknyttes på et hvilket som helst tidspunkt i prosessen, inkludert bokførte dokumenter og resulterende leverandør, kunde- og finansposter. Hvis du vil ha mer informasjon, kan du se [Behandle inngående dokumenter](across-process-income-documents.md).

## <a name="to-set-up-the-incoming-documents-feature"></a>Slik konfigurerer du funksjonen for inngående dokumenter:

1. Velg ikonet ![Lyspære som åpner Fortell meg-funksjonen](media/ui-search/search_small.png "Fortell hva du vil gjøre"), angi **Oppsett for inngående dokumenter**, og velg deretter den relaterte koblingen.
2. Fyll ut feltene etter behov. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

Som en del av oppsettet må du bestemme om du vil kreve godkjenning av innkommende dokumenter. Hvis du vil kreve godkjenning, må du definere godkjennere og arbeidsflyter for godkjenning. Hvis organisasjonen ikke vil kreve godkjenning, kan du hoppe over neste del.  

Hvis du bruker en tjeneste til å konvertere PDF-eller bildefiler som representerer inn kommende dokumenter, må du konfigurere det. Hvis ikke kan du også hoppe over den delen.  

## <a name="to-set-up-approvers-of-incoming-document-records"></a>Slik definerer du godkjennere av inngående dokumentposter:

Du kan eventuelt definere en godkjenningsprosess for innkommende dokumenter. Godkjennere av innkommende dokumenter må konfigureres som brukere av arbeidsflyt for godkjenning.

Før du kan opprette arbeidsflyter som omfatter godkjenningstrinn, må du definere arbeidsflytbrukerne som er involvert i godkjenningsprosessen. På siden **Brukeroppsett for godkjenning** angir du også beløpsgrenser for bestemte typer forespørsler og definerer stedfortredende godkjennere som godkjenningsforespørsler delegeres til når den opprinnelige godkjenneren er borte. Hvis du vil ha mer informasjon, kan du se [Konfigurere godkjenningsbrukere](across-how-to-set-up-approval-users.md).

## <a name="to-set-up-an-ocr-service"></a>Slik definerer du en OCR-tjeneste:

1. Velg ikonet ![Lyspære som åpner Fortell meg-funksjonen](media/ui-search/search_small.png "Fortell hva du vil gjøre"), angi **Oppsett for OCR-tjeneste**, og velg deretter den relaterte koblingen.
2. Fyll ut feltene etter behov. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

> [!NOTE]  
> Påloggingsdataene krypteres automatisk.

Hvis du vil ha mer informasjon, kan du se [Bruke OCR til å konvertere PDF- og bildefiler til elektroniske dokumenter](across-how-use-ocr-pdf-images-files.md).  

## <a name="see-also"></a>Se også

[Behandle inngående dokumenter](across-process-income-documents.md)  
[Inngående dokumenter](across-income-documents.md)  
[Innkjøp](purchasing-manage-purchasing.md)  
[Arbeide med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]