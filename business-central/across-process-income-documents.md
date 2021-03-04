---
title: Behandle inngående dokumenter | Microsoft-dokumentasjon
description: For å registrere et eksternt dokument i Business Central, for eksempel en PDF, må du først opprette eller fullføre en innkommende dokumentpost.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: electronic document, e-invoice, incoming document, OCR, ecommerce, document exchange, import invoice
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: bbec76297e32ec033d8f5c0fb0f24f54804ca532
ms.sourcegitcommit: 2e7307fbe1eb3b34d0ad9356226a19409054a402
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 12/17/2020
ms.locfileid: "4753078"
---
# <a name="processing-incoming-documents"></a>Behandle inngående dokumenter
For å registrere et eksternt dokument i [!INCLUDE[prod_short](includes/prod_short.md)] må du først opprette eller fullføre en innkommende dokumentpost. Du kan gjøre dette manuelt, eller du kan ta et bilde av det eksterne dokumentet og deretter opprette den inngående dokumentposten med bildefilen som vedlegg.

Fra PDF- eller bildefiler som du mottar fra handelspartnere, kan du få en ekstern OCR-tjeneste (optisk tegngjenkjenning) til å generere elektroniske dokumenter som kan konverteres til dokumentposter i [!INCLUDE[prod_short](includes/prod_short.md)]. Når du for eksempel mottar en faktura i PDF-format fra leverandøren, kan du sende den til OCR-tjenesten fra siden **Inngående dokumenter**. Du kan også sende filen til OCR-tjenesten i e-post. Deretter, når du får tilbake det elektroniske dokumentet, opprettes det automatisk en relatert innkommende dokumentpost. Etter noen sekunder vil du motta filen tilbake fra OCR-tjenesten som en elektronisk faktura som kan konverteres til en kjøpsfaktura for leverandøren.

| Hvis du vil | Se |
| --- | --- |
| Opprett poster for inngående dokument manuelt eller automatisk ved for eksempel å ta et bilde av en papirkvittering. |[Opprette innkommende dokumentposter](across-how-create-income-document-records.md) |
| Bruk for eksempel en OCR-tjeneste til å gjøre om PDF- og bildefiler til elektroniske dokumenter som kan konverteres til kjøpsfakturaer i [!INCLUDE[prod_short](includes/prod_short.md)]. Lære opp OCR-tjenesten for å unngå feil i neste gang den behandler liknende data. |[Bruke OCR til å konvertere PDF- og bildefiler til elektroniske dokumenter](across-how-use-ocr-pdf-images-files.md) |
| Tilknytte eller fjerne inngående dokumentposter for alle ikke-bokførte salgs- eller kjøpsdokumenter og til en hvilken som helst kunde, leverandør eller finanspost fra dokumentet eller posten. |[Opprette innkommende dokumentposter direkte fra dokumenter og poster](across-how-connect-disconnect-income-document-records.md) |
| Fra sidene **Kontoplan** og **Finansposter** bruker du søkefunksjonen til å finne finansposter for bokførte dokumenter som ikke har innkommende dokumentposter, og deretter sentralt koble eksisterende poster eller opprette nye med vedlagte dokumentfiler. |[Finne bokførte dokumenter uten innkommende dokumentposter](across-how-find-posted-documents-without-income-document-records.md) |
| Få bedre oversikt ved å sette inngående dokumentposter til Behandlet for å fjerne dem fra standardvisningen. |[Håndtere mange inngående dokumentposter](across-how-manage-many-income-document-records.md) |

## <a name="see-also"></a>Se også
[Inngående dokumenter](across-income-documents.md)  
[Innkjøp](purchasing-manage-purchasing.md)  
[Arbeide med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]