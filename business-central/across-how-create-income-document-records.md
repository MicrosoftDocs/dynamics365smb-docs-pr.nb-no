---
title: Opprette innkommende dokumentposter
description: Bruk ulike funksjoner på Innkommende dokumenter-siden til å gå gjennom utgiftskvitteringer, behandle OCR-oppgaver, konvertere innkommende dokumentfiler og legge ved eksterne filer.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: electronic document, e-invoice, incoming document, OCR, ecommerce, document exchange, import invoice
ms.date: 06/11/2021
ms.author: edupont
ms.openlocfilehash: cb7a16155c8055b9c4937843568f4e147cefc61b
ms.sourcegitcommit: ef80c461713fff1a75998766e7a4ed3a7c6121d0
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 02/15/2022
ms.locfileid: "8147297"
---
# <a name="create-incoming-document-records"></a>Opprett innkommende dokumentposter
På siden **Inngående dokumenter** kan du bruke forskjellige funksjoner til å se gjennom utgiftskvitteringer, behandle OCR-oppgaver og konvertere inngående dokumentfiler, manuelt eller automatisk, til de aktuelle dokumentene eller kladdelinjene. De eksterne filene kan tilknyttes på et hvilket som helst tidspunkt i prosessen, inkludert bokførte dokumenter og resulterende leverandør, kunde- og finansposter.

For å registrere et eksternt dokument i [!INCLUDE[prod_short](includes/prod_short.md)] må du først opprette eller fullføre en innkommende dokumentpost. Du kan gjøre dette manuelt, eller du kan ta et bilde av det eksterne dokumentet og deretter opprette den inngående dokumentposten med bildefilen som vedlegg.

Før du kan bruke funksjonen for inngående dokumenter, må du utføre den nødvendige konfigurasjonen. Hvis du vil ha mer informasjon, kan du se [Konfigurere inngående dokumenter](across-how-setup-income-documents.md).

## <a name="to-approve-or-reject-an-incoming-document"></a>Slik godkjenner eller avviser du et innkommende dokument
Hvis du vil tillate brukere å opprette fakturaer eller finanskladdelinjer fra innkommende dokumentposter med mindre de er godkjent, kan du definere godkjennere som må godkjenne postene før de kan behandles.

1. Velg ikonet ![Lyspære som åpner funksjonen Fortell meg.](media/ui-search/search_small.png "Fortell hva du vil gjøre") , angi **Innkommende dokumenter**, og velg deretter den relaterte koblingen.
2. Velg linjen med dokumentet som du vil godkjenne eller avvise, og velg deretter handlingen **Godkjenn** eller **Avvis**.

Hvis du godkjenner den inngående dokumentposten, merkes det av for **Frigitt** på linjen for det inngående dokumentet. Brukeren som for eksempel er ansvarlig for å opprette kjøpsfakturaer, kan fortsette å behandle posten.

## <a name="to-create-an-incoming-document-record-by-taking-a-photo"></a>Slik oppretter du en innkommende dokumentpost ved å ta et bilde
> [!NOTE]  
>   Fremgangsmåten nedenfor gjelder bare for nettbrett og telefoner med [!INCLUDE[prod_short](includes/prod_short.md)]-klienter.

1. I appfeltet velger du **Opprett innkommende dokument fra kamera**-flisen, og gå deretter til trinn 4.
2. Alternativt kan du velge Alternativer-knappen i appfeltet, velge **Innkommende dokumenter**, og deretter velge **Alle**.
3. På siden **Inngående dokumenter** velger du ellipseknappen, og deretter velger du **Opprett fra kamera**. Kameraet på tavle-PC-en eller telefon er aktivert.
4. Ta et bilde av et dokument, for eksempel et kjøpsmottak, som du vil behandle som et innkommende dokument, og velg deretter **OK**-knappen.

    En ny innkommende dokumentpost opprettes med bildet vedlagt.

## <a name="to-attach-an-image-to-an-incoming-document-record-by-taking-a-photo"></a>Slik legger du ved et bilde i en innkommende dokumentpost ved å ta et bilde
> [!NOTE]  
>   Fremgangsmåten nedenfor gjelder bare for nettbrett og telefoner med [!INCLUDE[prod_short](includes/prod_short.md)]-klienter.

1. Velg Alternativer-knappen i appfeltet, velg **Innkommende dokumenter**, og velg deretter **Alle**.
2. Åpne kortet for en eksisterende innkommende dokumentpost.
3. På siden **Inngående dokument** velger du ellipseknappen, og deretter velger du **Legg ved bilde fra kamera**. Kameraet på tavle-PC-en eller telefon er aktivert.
4. Ta et bilde av et dokument, for eksempel et kjøpsmottak, som du vil behandle som et innkommende dokument, og velg deretter **OK**-knappen.

    Bildet legges ved den innkommende dokumentposten.

## <a name="to-create-an-incoming-document-record-manually"></a>Slik oppretter du en innkommende dokumentpost manuelt:
1. Velg ikonet ![Lyspære som åpner funksjonen Fortell meg.](media/ui-search/search_small.png "Fortell hva du vil gjøre") , angi **Innkommende dokumenter**, og velg deretter den relaterte koblingen.
2. Velg handlingen **Opprett fra fil**.  
3. På siden **Sett inn fil** velger du en fil og deretter **Åpne**. Filen legges ved automatisk.
4. Du kan også velge handlingen **Ny**.
5. Hvis du vil legge ved en fil, velger du handlingen **Legg ved fil**.
6. På siden **Sett inn fil** velger du filen som representerer det innkommende dokumentet, og deretter velger du **Åpne**-knappen.
7. Fyll ut feltene etter behov på siden **Inngående dokument**. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

## <a name="see-also"></a>Se også
[Behandle inngående dokumenter](across-process-income-documents.md)  
[Inngående dokumenter](across-income-documents.md)  
[Innkjøp](purchasing-manage-purchasing.md)  
[Arbeide med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]