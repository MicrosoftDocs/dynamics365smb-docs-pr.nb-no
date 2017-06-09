---
title: "Opprette inngående dokumentposter| Microsoft-dokumentasjon"
description: Opprette innkommende dokumentposter
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: electronic document, e-invoice, incoming document, OCR, ecommerce, document exchange, import invoice
ms.date: 05/12/2016
ms.author: sgroespe
ms.translationtype: Human Translation
ms.sourcegitcommit: a31be0f9d07e2abb591e26f6bae34c6f6e4dcda6
ms.openlocfilehash: 38ea48e8a948df0fc3894e91d8393d2d14b2fd5a
ms.contentlocale: nb-no
ms.lasthandoff: 05/04/2017


---
# <a name="how-to-create-incoming-document-records"></a>Opprette innkommende dokumentposter
I vinduet **Inngående dokumenter** kan du bruke forskjellige funksjoner til å se gjennom utgiftskvitteringer, behandle OCR-oppgaver og konvertere inngående dokumentfiler, manuelt eller automatisk, til de aktuelle dokumentene eller kladdelinjene. De eksterne filene kan tilknyttes på et hvilket som helst tidspunkt i prosessen, inkludert bokførte dokumenter og resulterende leverandør, kunde- og finansposter.

For å registrere et eksternt dokument i [!INCLUDE[d365fin](includes/d365fin_md.md)] må du først opprette eller fullføre en innkommende dokumentpost. Du kan gjøre dette manuelt, eller du kan ta et bilde av det eksterne dokumentet og deretter opprette den inngående dokumentposten med bildefilen som vedlegg.

Før du kan bruke funksjonen for inngående dokumenter, må du utføre den nødvendige konfigurasjonen. Hvis du vil ha mer informasjon, kan du se [Konfigurere inngående dokumenter](across-how-setup-income-documents.md).

## <a name="to-approve-or-reject-an-incoming-document"></a>Slik godkjenner eller avviser du et innkommende dokument
Hvis du vil tillate brukere å opprette fakturaer eller finanskladdelinjer fra innkommende dokumentposter med mindre de er godkjent, kan du definere godkjennere som må godkjenne postene før de kan behandles.

1. I øvre høyre hjørne, velger du ikonet **Søk etter side eller en rapport** ![Søk etter side eller rapport](media/ui-search/search_small.png "ikonet Søk etter side eller rapport"), angi **Innkommende dokumenter**, og deretter velger du den beslektede koblingen.
2. Velg linjen med dokumentet som du vil godkjenne eller avvise, og velg deretter handlingen **Godkjenn** eller **Avvis**.

Hvis du godkjenner den inngående dokumentposten, merkes det av for **Frigitt** på linjen for det inngående dokumentet. Brukeren som for eksempel er ansvarlig for å opprette kjøpsfakturaer, kan fortsette å behandle posten.

## <a name="to-create-an-incoming-document-record-by-taking-a-photo"></a>Slik oppretter du en innkommende dokumentpost ved å ta et bilde
**Merk**: Fremgangsmåten nedenfor gjelder bare for nettbrett og telefoner med [!INCLUDE[d365fin](includes/d365fin_md.md)]-klienter.

1. I appfeltet velger du **Opprett innkommende dokument fra kamera**-flisen, og gå deretter til trinn 4.
2. Alternativt kan du velge Alternativer-knappen i appfeltet, velge **Innkommende dokumenter**, og deretter velge **Alle**.
3. I vinduet **Inngående dokumenter** velger du ellipseknappen, og deretter velger du **Opprett fra kamera**. Kameraet på tavle-PC-en eller telefon er aktivert.
4. Ta et bilde av et dokument, for eksempel et kjøpsmottak, som du vil behandle som et innkommende dokument, og velg deretter **OK**-knappen.

En ny innkommende dokumentpost opprettes med bildet vedlagt.

## <a name="to-attach-an-image-to-an-incoming-document-record-by-taking-a-photo"></a>Slik legger du ved et bilde i en innkommende dokumentpost ved å ta et bilde
**Merk**: Fremgangsmåten nedenfor gjelder bare for nettbrett og telefoner med [!INCLUDE[d365fin](includes/d365fin_md.md)]-klienter.

1. Velg Alternativer-knappen i appfeltet, velg **Innkommende dokumenter**, og velg deretter **Alle**.
2. Åpne kortet for en eksisterende innkommende dokumentpost.
3. I vinduet **Inngående dokument** velger du ellipseknappen, og deretter velger du **Legg ved bilde fra kamera**. Kameraet på tavle-PC-en eller telefon er aktivert.
4. Ta et bilde av et dokument, for eksempel et kjøpsmottak, som du vil behandle som et innkommende dokument, og velg deretter **OK**-knappen.

Bildet legges ved den innkommende dokumentposten.

## <a name="to-create-an-incoming-document-record-manually"></a>Slik oppretter du en innkommende dokumentpost manuelt:
1. I øvre høyre hjørne, velger du ikonet **Søk etter side eller en rapport** ![Søk etter side eller rapport](media/ui-search/search_small.png "ikonet Søk etter side eller rapport"), angi **Innkommende dokumenter**, og deretter velger du den beslektede koblingen.
2. Velg handlingen **Opprett fra fil**.  
3. I **Sett inn fil**-vinduet velger du en fil og deretter **Åpne**.

    Filen legges ved automatisk.
4. Du kan også velge handlingen **Ny**.
5. Hvis du vil legge ved en fil, velger du handlingen **Legg ved fil**.
6. I vinduet **Sett inn fil** velger du filen som representerer det innkommende dokumentet, og deretter velger du **Åpne**- knappen.
7. Fyll ut feltene etter behov i vinduet **Inngående dokument**. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

## <a name="see-also"></a>Se også
[Behandle inngående dokumenter](across-process-income-documents.md)  
[Inngående dokumenter](across-income-documents.md)  
[Innkjøp](purchasing-manage-purchasing.md)  
[Arbeide med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

