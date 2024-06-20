---
title: Oversikt over oppgaver for å håndtere kjøp
description: 'Gir oversikt over oppgaver for å håndtere kjøp eller innkjøpsprosesser, inkludert hvordan kjøpsfakturaer og bestillinger fungerer.'
author: brentholtorf
ms.topic: overview
ms.devlang: al
ms.search.keywords: 'procurement, supply, vendor order'
ms.search.form: '460, 9307'
ms.date: 03/21/2024
ms.author: bholtorf
ms.service: dynamics-365-business-central
ms.reviewer: bholtorf
---
# <a name="purchasing"></a>Kjøp

Du kan opprette en kjøpsfaktura eller bestilling for å registrere kjøpskostnader og spore leverandørgjeld. Hvis du vil kontrollere en beholdning, brukes kjøpsfakturaer også til å oppdatere lagernivåer dynamisk, slik at du kan redusere lagerkostnadene og gi bedre kundeservice. Kjøpskostnadene, inkludert tjenesteutgifter samt lagerverdier som er resultat av bokføring av kjøpsfakturaer, bidrar til fortjenestetall og andre økonomiske KPIer i rollesenteret.

Du må bruke bestillinger hvis kjøpsprosessen krever at du registrerer delvise mottak av et bestillingsantall, for eksempel fordi det fullstendige antallet ikke var tilgjengelig hos leverandøren. Hvis du selger varer ved å levere direkte fra leverandøren til kunden, som en direkte levering, må du også å bruke bestillinger. Hvis du vil ha mer informasjon, kan du se [Foreta direkte leveringer](sales-how-drop-shipment.md). I alle andre henseender fungerer bestillinger på samme måte som kjøpsfakturaer.

Du kan opprette kjøpsfakturaer automatisk ved hjelp av OCR-tjenesten (Optical Character Recognition) for å konvertere PDF-fakturaer fra leverandører til elektroniske dokumenter, som deretter konverteres til kjøpsfakturaer ved hjelp av en arbeidsflyt. Hvis du vil bruke denne funksjonaliteten, må du først registrere deg for OCR-tjenesten og deretter utføre ulike oppsett. Hvis du vil ha mer informasjon, kan du se [Innkommende dokumenter](across-income-documents.md).

Produkter kan være både varer og tjenester. Hvis du vil ha mer informasjon, kan du se [Registrere nye varer](inventory-how-register-new-items.md).

Du kan inkludere en godkjenningsarbeidsflyt for alle innkjøpsprosesser, for eksempel hvis du vil kreve at store innkjøp godkjennes av regnskapssjefen. Hvis du vil ha mer informasjon, kan du se [Bruke godkjenningsarbeidsflyter](across-how-use-approval-workflows.md).

Delen nedenfor beskriver en sekvens av oppgaver og har koblinger til artiklene som beskriver dem.

## <a name="get-started-with-purchase-capabilities"></a>Kom i gang med kjøpsfunksjoner

Før du kjøper varer, må du angi hvordan du vil håndtere selskapets kjøpsprosesser.

|Til ...| Se |
|---|---|
| Konfigurere reglene og verdiene som definerer selskapets innkjøpspolicyer. | [Konfigurer kjøp](purchasing-setup-purchasing.md) |
| Registrer hver leverandør du kjøper fra, med et leverandørkort. | [Registrer nye leverandører](purchasing-how-register-new-vendors.md) |

## <a name="purchase-analytics"></a>Kjøpsanalyse

Denne delen beskriver analyseverktøyene du kan bruke til å få innsikt i kjøpsprosessene.

| Til ... | Se |
| --- | --- |
| Finn ut mer om muligheter for analyse av kjøpsdata. | [Oversikt over kjøpsanalyse](purchasing-analytics-overview.md) |
| Utfør ad hoc-analyse av kjøpsdata direkte på listesider og spørringer. | [Ad hoc-analyse av kjøpsdata](ad-hoc-analysis-purchasing.md) |
| Utforsk innebygde kjøpsrapporter. | [Innebygde kjøpsrapporter](purchase-reports.md) |

## <a name="quote-to-order-to-purchase-invoice"></a>Gi tilbud for å bestille til kjøpsfaktura

Tabellen nedenfor beskriver hvordan du bruker enkle kjøpsprosesser.

| Til | Se |
| --- | --- |
|Opprett en forespørsel for å gjenspeile en forespørsel om tilbud fra leverandøren, som du senere kan konvertere til en bestilling.|[Be om tilbud](purchasing-how-request-quotes.md)|
| Opprett en kjøpsfaktura for alle eller merkede linjer i en salgsfaktura. |[Kjøpvarer for et salg](purchasing-how-purchase-products-sale.md) |
| Opprett en kjøpsfaktura for å registrere avtalen med en leverandør om å kjøpe produkter på bestemte leverings- og betalingsbetingelser. |[Registrer kjøp](purchasing-how-record-purchases.md) |
| Lære hvordan [!INCLUDE[prod_short](includes/prod_short.md)] beregner når du må bestille en vare for å motta den på en bestemt dato.|[Beregn dato for kjøp](purchasing-date-calculation-for-purchases.md)|
|Forstå hva som skjer når du bokfører kjøpsdokumenter.|[Bokføre kjøp](ui-post-purchases.md)|

Hvis du trenger mer komplekse kjøpsprosesser, inneholder tabellen nedenfor artikler som forklarer hva du kan gjøre med [!INCLUDE[prod_short](includes/prod_short.md)].

| Til | Se |
| --- | --- |
| Utfør en handling på en ubetalt bokført kjøpsfaktura for å opprette en kreditnota automatisk og enten annullere kjøpsfakturaen eller opprette den på nytt, slik at du kan foreta korrigeringer. |[Korrigere eller annullere ubetalte salgsfakturaer](purchasing-how-correct-cancel-unpaid-purchase-invoices.md) |
| Opprett en kjøpskreditnota for å tilbakestille en bestemt bokført kjøpsfaktura for å vise hvilke produkter du vil returnere til leverandøren, og hvilket betalingsbeløp du vil kreve inn. |[Behandle bestillingsreturer eller annulleringer](purchasing-how-process-purchase-returns-cancellations.md) |
|Håndter forpliktelsen din til en leverandør om å kjøpe store antall levert i flere forsendelser over tid.|[Arbeid med rammebestillinger](sales-how-to-create-blanket-sales-orders.md)|


## <a name="canceled-orders-refunds-and-returns"></a>Kansellerte bestillinger, refusjoner og returer

Tabellen nedenfor beskriver hvordan du håndterer kansellerte bestillinger, refusjoner og returer av varer du kjøper.

| Til | Se |
| --- | --- |
|Forbered fakturering av flere mottak fra samme leverandør én gang ved å kombinere mottakene på en faktura.|[Kombinere mottak på én faktura](purchasing-how-to-combine-receipts.md)|
|Konverter for eksempel elektroniske fakturaer fra leverandører til kjøpsfakturaer i Business Central.|[Motta og konverter elektroniske dokumenter](purchasing-how-to-receive-and-convert-electronic-documents.md)|


## <a name="other-processes-in-sales"></a>Andre salgsprosesser

Tabellen nedenfor beskriver hvordan du håndterer andre kjøpsprosesser.

| Til | Se |
| --- | --- |
|Løs forvirring når det finnes to eller flere poster for samme leverandør.|[Slå sammen dupliserte poster](sales-how-merge-duplicate-records.md)|


## <a name="external-document-numbers"></a>Eksterne dokumentnumre

[!INCLUDE [ext-doc-no-purch](includes/ext-doc-no-purch.md)]

## <a name="see-also"></a>Se også

[Definere kjøp](purchasing-setup-purchasing.md)  
[Registrer nye leverandører](purchasing-how-register-new-vendors.md)  
[Oversikt over kjøpsanalyse](purchasing-analytics-overview.md)   
[Administrere skyldige beløp](payables-manage-payables.md)  
[Arbeid med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  
[Generelle forretningsfunksjoner](ui-across-business-areas.md)

## [!INCLUDE[prod_short](includes/free_trial_md.md)]  


[!INCLUDE[footer-include](includes/footer-banner.md)]
