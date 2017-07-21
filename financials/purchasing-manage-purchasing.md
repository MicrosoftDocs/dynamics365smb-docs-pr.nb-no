---
title: "Oversikt over oppgaver for å håndtere kjøp | Microsoft-dokumentasjon"
description: "Gir oversikt over oppgaver for å håndtere kjøp eller innkjøpsprosesser, inkludert hvordan kjøpsfakturaer og bestillinger fungerer."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: procurement, supply, vendor order
ms.date: 03/29/2017
ms.author: sgroespe
ms.translationtype: Human Translation
ms.sourcegitcommit: 81636fc2e661bd9b07c54da1cd5d0d27e30d01a2
ms.openlocfilehash: 653cd9b5e9651f2039ab18f3e7a26b299238d817
ms.contentlocale: nb-no
ms.lasthandoff: 07/07/2017


---
# <a name="purchasing"></a>Kjøp
Du kan opprette en kjøpsfaktura eller bestilling for å registrere kjøpskostnader og spore leverandørgjeld. Hvis du vil kontrollere en beholdning, brukes kjøpsfakturaer også til å oppdatere lagernivåer dynamisk, slik at du kan redusere lagerkostnadene og gi bedre kundeservice. Kjøpskostnadene, inkludert tjenesteutgifter samt lagerverdier som er resultat av bokføring av kjøpsfakturaer, bidrar til fortjenestetall og andre økonomiske KPI-er på Hjem-siden.

Du må bruke bestillinger hvis kjøpsprosessen krever at du registrerer delvise mottak av et bestillingsantall, for eksempel fordi det fullstendige antallet ikke var tilgjengelig hos leverandøren. Hvis du selger varer ved å levere direkte fra leverandøren til kunden, som en direkte levering, må du også å bruke bestillinger. Hvis du vil ha mer informasjon, kan du se [Foreta direkte leveringer](sales-how-drop-shipment.md). I alle andre henseender fungerer bestillinger på samme måte som kjøpsfakturaer.

Du kan opprette kjøpsfakturaer automatisk ved hjelp av OCR-tjenesten (Optical Character Recognition) for å konvertere PDF-fakturaer fra leverandører til elektroniske dokumenter, som deretter konverteres til kjøpsfakturaer ved hjelp av en arbeidsflyt. Hvis du vil bruke denne funksjonaliteten, må du først registrere deg for OCR-tjenesten og deretter utføre ulike oppsett. Hvis du vil ha mer informasjon, kan du se [Behandle inngående dokumenter](across-process-income-documents.md).      

Produkter kan være både varer og tjenester. Hvis du vil ha mer informasjon, kan du se [Registrere nye varer](inventory-how-register-new-items.md).

Du kan inkludere en godkjenningsarbeidsflyt for alle innkjøpsprosesser, for eksempel hvis du vil kreve at store innkjøp godkjennes av regnskapssjefen. Hvis du vil ha mer informasjon, kan du se [Bruke godkjenningsarbeidsflyter](across-how-use-approval-workflows.md).

Tabellen nedenfor beskriver en sekvens av oppgaver, og har koblinger til emnene som beskriver dem. Disse oppgavene vises i rekkefølgen de vanligvis utføres i.

| Hvis du vil | Se |
| --- | --- |
| Opprett en kjøpsfaktura for å registrere avtalen med en leverandør om å kjøpe produkter på bestemte leverings- og betalingsbetingelser. |[Registrere kjøp](purchasing-how-record-purchases.md) |
| Opprett en kjøpsfaktura for alle eller merkede linjer i en salgsfaktura. |[Kjøpe varer for salg](purchasing-how-purchase-products-sale.md) |
| Utfør en handling på en ubetalt bokført kjøpsfaktura for å opprette en kreditnota automatisk og enten annullere kjøpsfakturaen eller opprette den på nytt, slik at du kan foreta korrigeringer. |[Korrigere eller annullere ubetalte salgsfakturaer](purchasing-how-correct-cancel-unpaid-purchase-invoices.md) |
| Opprett en kjøpskreditnota for å tilbakestille en bestemt bokført kjøpsfaktura for å vise hvilke produkter du vil returnere til leverandøren, og hvilket betalingsbeløp du vil kreve inn. |[Behandle bestillingsreturer eller annulleringer](purchasing-how-register-new-vendors.md) |
| Opprett et leverandørkort for hver leverandør som du kjøper fra. |[Registrere nye leverandører](purchasing-how-register-new-vendors.md) |

## <a name="see-also"></a>Se også
[Definere kjøp](purchasing-setup-purchasing.md)  
[Administrere skyldige beløp](payables-manage-payables.md)  
[Administrere prosjekter](projects-manage-projects.md)    
[Forsyningskjede](madeira-supply-chain.md)      
[Arbeide med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)  
[Generelle forretningsfunksjoner](ui-across-business-areas.md)

## [!INCLUDE[d365fin](includes/free_trial_md.md)]
