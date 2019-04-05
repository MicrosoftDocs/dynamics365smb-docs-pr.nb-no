---
title: Oversikt over oppgaver for å håndtere kjøp | Microsoft-dokumentasjon
description: Gir oversikt over oppgaver for å håndtere kjøp eller innkjøpsprosesser, inkludert hvordan kjøpsfakturaer og bestillinger fungerer.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: procurement, supply, vendor order
ms.date: 11/15/2018
ms.author: sgroespe
ms.openlocfilehash: 87e3d134abe82e0f55acf4d3680b84fbc2c0c14b
ms.sourcegitcommit: 1bcfaa99ea302e6b84b8361ca02730b135557fc1
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 03/08/2019
ms.locfileid: "802613"
---
# <a name="purchasing"></a>Kjøp
Du kan opprette en kjøpsfaktura eller bestilling for å registrere kjøpskostnader og spore leverandørgjeld. Hvis du vil kontrollere en beholdning, brukes kjøpsfakturaer også til å oppdatere lagernivåer dynamisk, slik at du kan redusere lagerkostnadene og gi bedre kundeservice. Kjøpskostnadene, inkludert tjenesteutgifter samt lagerverdier som er resultat av bokføring av kjøpsfakturaer, bidrar til fortjenestetall og andre økonomiske KPIer i rollesenteret.

Du må bruke bestillinger hvis kjøpsprosessen krever at du registrerer delvise mottak av et bestillingsantall, for eksempel fordi det fullstendige antallet ikke var tilgjengelig hos leverandøren. Hvis du selger varer ved å levere direkte fra leverandøren til kunden, som en direkte levering, må du også å bruke bestillinger. Hvis du vil ha mer informasjon, kan du se [Foreta direkte leveringer](sales-how-drop-shipment.md). I alle andre henseender fungerer bestillinger på samme måte som kjøpsfakturaer.

Du kan opprette kjøpsfakturaer automatisk ved hjelp av OCR-tjenesten (Optical Character Recognition) for å konvertere PDF-fakturaer fra leverandører til elektroniske dokumenter, som deretter konverteres til kjøpsfakturaer ved hjelp av en arbeidsflyt. Hvis du vil bruke denne funksjonaliteten, må du først registrere deg for OCR-tjenesten og deretter utføre ulike oppsett. Hvis du vil ha mer informasjon, kan du se [Behandle inngående dokumenter](across-process-income-documents.md).      

Produkter kan være både varer og tjenester. Hvis du vil ha mer informasjon, kan du se [Registrere nye varer](inventory-how-register-new-items.md).

Du kan inkludere en godkjenningsarbeidsflyt for alle innkjøpsprosesser, for eksempel hvis du vil kreve at store innkjøp godkjennes av regnskapssjefen. Hvis du vil ha mer informasjon, kan du se [Bruke godkjenningsarbeidsflyter](across-how-use-approval-workflows.md).

Tabellen nedenfor beskriver en sekvens av oppgaver, og har koblinger til emnene som beskriver dem.

| Til | Se |
| --- | --- |
| Opprett en kjøpsfaktura for å registrere avtalen med en leverandør om å kjøpe produkter på bestemte leverings- og betalingsbetingelser. |[Registrere kjøp](purchasing-how-record-purchases.md) |
|Opprett en forespørsel for å gjenspeile en forespørsel om tilbud fra leverandøren, som du senere kan konvertere til en bestilling.|[Be om tilbud](purchasing-how-request-quotes.md)|
| Opprett en kjøpsfaktura for alle eller merkede linjer i en salgsfaktura. |[Kjøpe varer for salg](purchasing-how-purchase-products-sale.md) |
| Utfør en handling på en ubetalt bokført kjøpsfaktura for å opprette en kreditnota automatisk og enten annullere kjøpsfakturaen eller opprette den på nytt, slik at du kan foreta korrigeringer. |[Korrigere eller annullere ubetalte salgsfakturaer](purchasing-how-correct-cancel-unpaid-purchase-invoices.md) |
| Opprett en kjøpskreditnota for å tilbakestille en bestemt bokført kjøpsfaktura for å vise hvilke produkter du vil returnere til leverandøren, og hvilket betalingsbeløp du vil kreve inn. |[Behandle bestillingsreturer eller annulleringer](purchasing-how-register-new-vendors.md) |
|Forbered fakturering av flere mottak fra samme leverandør én gang ved å kombinere mottakene på en faktura.|[Kombinere mottak på én faktura](purchasing-how-to-combine-receipts.md)|
|Konverter for eksempel elektroniske fakturaer fra leverandører til kjøpsfakturaer i Business Central.|[Motta og konvertere elektroniske dokumenter](purchasing-how-to-receive-and-convert-electronic-documents.md)|
| Lære hvordan [!INCLUDE[d365fin](includes/d365fin_md.md)] beregner når du må bestille en vare for å motta den på en bestemt dato.|[Beregne dato for kjøp](purchasing-date-calculation-for-purchases.md)|

## <a name="see-also"></a>Se også
[Definere kjøp](purchasing-setup-purchasing.md)  
[Registrere nye leverandører](purchasing-how-register-new-vendors.md)  
[Administrere skyldige beløp](payables-manage-payables.md)  
[Administrere prosjekter](projects-manage-projects.md)    
[Arbeide med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)  
[Generelle forretningsfunksjoner](ui-across-business-areas.md)

## [!INCLUDE[d365fin](includes/free_trial_md.md)]  
