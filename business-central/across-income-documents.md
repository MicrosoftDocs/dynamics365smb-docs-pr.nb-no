---
title: Arbeide med innkommende dokumenter | Microsoft-dokumentasjon
description: Du kan behandle innkommende eksterne forretningsdokumenter, for eksempel kvitteringer eller PDF-filer, behandle OCR-oppgaver og konvertere filer til elektroniske dokumenter og poster.
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: electronic document, e-invoice, incoming document, OCR, ecommerce, document exchange, import invoice
ms.date: 10/01/2018
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 33b900f1ac9e295921e7f3d6ea72cc93939d8a1b
ms.openlocfilehash: 989fff07cb0608b8dbf6611a39163fc3cfe31459
ms.contentlocale: nb-no
ms.lasthandoff: 11/26/2018

---
# <a name="incoming-documents"></a>Inngående dokumenter
Noen forretningstransaksjoner er ikke registrert i [!INCLUDE[d365fin](includes/d365fin_md.md)] fra starten. I stedet sendes et eksternt forretningsdokument til selskapet ditt som et e-postvedlegg eller en kopi som du skanner til fil. Dette er vanlig for kjøp, hvor slike innkommende dokumentfiler representerer kvitteringer for utgifter eller små innkjøp.

Fra PDF- eller bildefiler som representerer innkommende dokumenter, kan du få en ekstern OCR-tjeneste (optisk tegngjenkjenning) til å generere elektroniske dokumenter som deretter kan konverteres til dokumentposter i [!INCLUDE[d365fin](includes/d365fin_md.md)].

På siden **Inngående dokumenter** kan du bruke forskjellige funksjoner til å se gjennom utgiftskvitteringer, behandle OCR-oppgaver og konvertere inngående dokumentfiler, manuelt eller automatisk, til de aktuelle dokumentene eller kladdelinjene. De eksterne filene kan tilknyttes på et hvilket som helst tidspunkt i prosessen, inkludert bokførte dokumenter og resulterende leverandør, kunde- og finansposter.

Prosessen for inngående dokumenter kan bestå av følgende hovedaktiviteter:

* Registrere de eksterne dokumentene i [!INCLUDE[d365fin](includes/d365fin_md.md)] ved å opprette linjer på siden **Inngående dokumenter** på én av følgende måter:
  * Manuelt, ved å bruke enkle funksjoner fra en PC eller en mobil enhet, på en av følgende måter:
    * Bruk **Opprett fra fil**-knappen, og fyll deretter ut aktuelle felt på siden **Inngående dokument**. Filen legges ved automatisk.  
    * Bruk **Ny**-knappen, og fyll deretter ut aktuelle felt på siden **Inngående dokument**, og legg manuelt ved den relaterte filen.
    * Fra et nettverk eller en telefon kan du bruke **Opprett fra kamera**-knappen til å opprette en ny innkommende dokumentpost, og deretter sende bildet til OCR-tjenesten, for eksempel.
  * Automatisk, ved å motta dokumentet fra OCR-tjenesten som et elektronisk dokument etter at du har sendt den relaterte PDF- eller bildefilen til OCR-tjenesten. Hurtigfanen **Økonomisk informasjon** fylles ut automatisk på siden **Inngående dokument**.
* Bruk OCR-tjenesten for å konvertere PDF- eller bildefiler til elektroniske dokumenter som kan konverteres til dokumentposter i [!INCLUDE[d365fin](includes/d365fin_md.md)].
* Opprett nye dokumenter eller finanskladdelinje for inngående dokumentposter ved å skrive inn informasjonen mens du leser den fra inngående dokumentfiler.
* Knytte inngående dokumentfiler til salgs- og kjøpsdokumenter med en hvilken som helst status, inkludert til leverandør, kunde- og finansposter som resultat av bokføring.
* Vise innkommende dokumentposter og tilhørende vedlegg fra alle kjøps- og salgsdokument eller oppføringer, eller søke etter alle finansposter uten innkommende dokumentposter fra siden **Kontoplan**.

| Til | Se |
| --- | --- |
| Definere funksjonen for inngående dokumenter og OCR-tjenesten. |[Konfigurere inngående dokumenter](across-how-setup-income-documents.md) |
| Opprett innkommende dokumentposter, legg ved filer eller bruk OCR til å konvertere PDF-filer til elektroniske dokumenter, konverter elektroniske dokumenter til dokumentposter, overvåk innkommende dokumentposter og bokførte salgs- og kjøpsdokumenter. |[Behandle inngående dokumenter](across-process-income-documents.md) |

## <a name="see-also"></a>Se også
[Innkjøp](purchasing-manage-purchasing.md)  
[Arbeide med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

