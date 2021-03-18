---
title: Arbeide med innkommende dokumenter | Microsoft-dokumentasjon
description: Du kan behandle innkommende eksterne forretningsdokumenter, for eksempel kvitteringer eller PDF-filer, behandle OCR-oppgaver og konvertere filer til elektroniske dokumenter og poster.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: electronic document, e-invoice, incoming document, OCR, ecommerce, document exchange, import invoice
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: 938a86f316e494c0b64e5f2853ee64b9fb5064d8
ms.sourcegitcommit: ff2b55b7e790447e0c1fcd5c2ec7f7610338ebaa
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 02/15/2021
ms.locfileid: "5379226"
---
# <a name="incoming-documents"></a>Inngående dokumenter

Noen forretningstransaksjoner er ikke registrert i [!INCLUDE[prod_short](includes/prod_short.md)] fra starten. I stedet sendes et eksternt forretningsdokument til selskapet ditt som et e-postvedlegg eller en kopi som du skanner til fil. Dette er vanlig for kjøp, hvor slike innkommende dokumentfiler representerer kvitteringer for utgifter eller små innkjøp.

Fra PDF- eller bildefiler som representerer innkommende dokumenter, kan du få en ekstern OCR-tjeneste (optisk tegngjenkjenning) til å generere elektroniske dokumenter som deretter kan konverteres til dokumentposter i [!INCLUDE[prod_short](includes/prod_short.md)]. Velg en tjenestepakke som passer for organisasjonen og/eller landet/området. Du kan også opprette poster manuelt for å representere de eksterne dokumentene.  

På siden **Inngående dokumenter** kan du bruke forskjellige funksjoner til å se gjennom utgiftskvitteringer, behandle OCR-oppgaver og konvertere inngående dokumentfiler, manuelt eller automatisk, til de aktuelle dokumentene eller kladdelinjene. De eksterne filene kan tilknyttes på et hvilket som helst tidspunkt i prosessen, inkludert bokførte dokumenter og resulterende leverandør, kunde- og finansposter.

Prosessen for inngående dokumenter kan bestå av følgende hovedaktiviteter:

* Registrere de eksterne dokumentene i [!INCLUDE[prod_short](includes/prod_short.md)] ved å opprette linjer på siden **Inngående dokumenter** på én av følgende måter:
  * Manuelt, ved å bruke enkle funksjoner fra en PC eller en mobil enhet, på en av følgende måter:
    * Bruk **Opprett fra fil**-knappen, og fyll deretter ut aktuelle felt på siden **Inngående dokument**. Filen legges ved automatisk.  
    * Bruk **Ny**-knappen, og fyll deretter ut aktuelle felt på siden **Inngående dokument**, og legg manuelt ved den relaterte filen.
    * Fra et nettverk eller en telefon kan du bruke **Opprett fra kamera**-knappen til å opprette en ny innkommende dokumentpost, og deretter sende bildet til OCR-tjenesten, for eksempel.
  * Automatisk, ved å motta dokumentet fra OCR-tjenesten som et elektronisk dokument etter at du har sendt den relaterte PDF- eller bildefilen til OCR-tjenesten. Hurtigfanen **Økonomisk informasjon** fylles ut automatisk på siden **Inngående dokument**.
* Bruk OCR-tjenesten for å konvertere PDF- eller bildefiler til elektroniske dokumenter som kan konverteres til dokumentposter i [!INCLUDE[prod_short](includes/prod_short.md)].
* Opprett nye dokumenter eller finanskladdelinje for inngående dokumentposter ved å skrive inn informasjonen mens du leser den fra inngående dokumentfiler.
* Knytte inngående dokumentfiler til salgs- og kjøpsdokumenter med en hvilken som helst status, inkludert til leverandør, kunde- og finansposter som resultat av bokføring.
* Vise innkommende dokumentposter og tilhørende vedlegg fra alle kjøps- og salgsdokument eller oppføringer, eller søke etter alle finansposter uten innkommende dokumentposter fra siden **Kontoplan**.

| Til | Se |
| --- | --- |
| Definere funksjonen for inngående dokumenter og OCR-tjenesten. |[Konfigurere inngående dokumenter](across-how-setup-income-documents.md) |
| Opprett innkommende dokumentposter, legg ved filer eller bruk OCR til å konvertere PDF-filer til elektroniske dokumenter, konverter elektroniske dokumenter til dokumentposter, overvåk innkommende dokumentposter og bokførte salgs- og kjøpsdokumenter. |[Behandle inngående dokumenter](across-process-income-documents.md) |

## <a name="see-related-training-at-microsoft-learn"></a>Se relatert opplæring på [Microsoft Learn](/learn/modules/incoming-documents-dynamics-365-business-central/index)

## <a name="see-also"></a>Se også

[Innkjøp](purchasing-manage-purchasing.md)  
[Arbeide med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]