---
title: Konfigurere inngående dokumenter
description: 'Konfigurer funksjonen Innkommende dokumenter til å opprette elektroniske dokumenter, behandle OCR-oppgaver, importere fakturaer og konvertere bildefiler.'
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 'electronic document, e-invoice, incoming document, OCR, ecommerce, document exchange, import invoice'
ms.date: 06/14/2022
ms.author: edupont
---
# <a name="set-up-incoming-documents"></a><a name="set-up-incoming-documents"></a>Konfigurere inngående dokumenter

Hvis du oppretter finanskladdelinjer fra innkommende dokumentposter, må du angi hvilken kladdemal og kladd som skal brukes på siden **Oppsett for inngående dokumenter**.

Når funksjonen for **innkommende dokumenter** er konfigurert, kan du bruke forskjellige funksjoner til å se gjennom utgiftskvitteringer, behandle OCR-oppgaver og konvertere innkommende dokumentfiler, manuelt eller automatisk, til de aktuelle dokumentene eller kladdelinjene. De eksterne filene kan tilknyttes på et hvilket som helst tidspunkt i prosessen, inkludert bokførte dokumenter og resulterende leverandør, kunde- og finansposter. Hvis du vil ha mer informasjon, kan du se [Opprett innkommende dokumentposter](across-how-create-income-document-records.md).

## <a name="to-set-up-the-incoming-documents-feature"></a><a name="to-set-up-the-incoming-documents-feature"></a>Slik konfigurerer du funksjonen for inngående dokumenter:

1. Velg ikonet ![Lyspære som åpner funksjonen Fortell meg.](media/ui-search/search_small.png "Fortell hva du vil gjøre") , angi **Innkommende dokumentoppsett**, og velg deretter den relaterte koblingen.
2. Fyll ut feltene etter behov. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

Som en del av oppsettet må du bestemme om du vil kreve godkjenning av innkommende dokumenter. Hvis du vil kreve godkjenning, må du [definere godkjennere og arbeidsflyter for godkjenning](#to-set-up-approvers-of-incoming-document-records). Hvis organisasjonen ikke vil kreve godkjenning, kan du hoppe over neste del.

Hvis du bruker en OCR-tjeneste til å konvertere PDF-eller bildefiler som representerer inn kommende dokumenter, [må du konfigurere det](#to-set-up-an-ocr-service). Hvis ikke kan du også hoppe over den delen.

## <a name="to-set-up-approvers-of-incoming-document-records"></a><a name="to-set-up-approvers-of-incoming-document-records"></a>Slik definerer du godkjennere av inngående dokumentposter:

Hvis du ikke vil at brukerne skal opprette fakturaer eller finanskladdelinjer fra innkommende dokumentposter med mindre dokumentene først er godkjent, må du definere en godkjenningsprosess for innkommende dokumenter. Godkjennere av innkommende dokumenter må konfigureres som brukere av arbeidsflyt for godkjenning.

Før du kan opprette arbeidsflyter som omfatter godkjenningstrinn, må du definere arbeidsflytbrukerne som er involvert i godkjenningsprosessen. På siden **Brukeroppsett for godkjenning** angir du også beløpsgrenser for bestemte typer forespørsler og definerer stedfortredende godkjennere som godkjenningsforespørsler delegeres til når den opprinnelige godkjenneren er borte. Hvis du vil ha mer informasjon, kan du se [Konfigurere godkjenningsbrukere](across-how-to-set-up-approval-users.md).

## <a name="to-set-up-an-ocr-service"></a><a name="to-set-up-an-ocr-service"></a>Slik definerer du en OCR-tjeneste:

Du kan aktivere PDF- og bildefiler i elektroniske dokumenter som du kan konvertere til fakturaer, kreditnotaer eller kladdelinjer, ved å definere OCR-funksjonen. Du kan også opprette poster manuelt for å representere de eksterne dokumentene.

1. Velg ikonet ![Lyspære som åpner funksjonen Fortell meg.](media/ui-search/search_small.png "Fortell hva du vil gjøre") , angi **Oppsett for OCR-tjeneste**, og velg deretter den relaterte koblingen.
2. Fyll ut feltene etter behov. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

> [!NOTE]  
> Påloggingsdataene krypteres automatisk.

Hvis du vil ha mer informasjon, kan du se [Bruke OCR til å konvertere PDF- og bildefiler til elektroniske dokumenter](across-how-use-ocr-pdf-images-files.md).  

## <a name="see-related-microsoft-training"></a><a name="see-related-microsoft-training"></a>Se relatert [Microsoft-opplæring](/training/modules/incoming-documents-dynamics-365-business-central/)

## <a name="see-also"></a><a name="see-also"></a>Se også

[Inngående dokumenter](across-income-documents.md)  
[Innkjøp](purchasing-manage-purchasing.md)  
[Arbeid med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]
