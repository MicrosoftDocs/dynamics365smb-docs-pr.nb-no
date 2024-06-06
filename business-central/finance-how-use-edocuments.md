---
title: Bruk e-dokumenter i salg
description: Lær hvordan du bruker funksjoner for e-dokumenter som er knyttet til salg.
author: altotovi
ms.topic: conceptual
ms.devlang: al
ms.search.keywords: 'electronic document, electronic invoice, e-document, e-invoice, sales, deliver'
ms.search.form: '42, 43, 132, 6103, 6133, 6121, 9301, 9305'
ms.date: 04/10/2024
ms.author: altotovi
ms.service: dynamics-365-business-central
---

# <a name="use-e-documents-in-the-sales-process"></a>Bruk e-dokumenter i salgsprosessen

Du kan bruke konfigurerte elektroniske dokumenter (e-dokumenter) med salgsdokumentene.

Du kan bruke følgende salgsdokumenter med e-dokumentfunksjonalitet:  

- Salgsfakturaer
- Ordrer
- Salgskreditnotaer
- Servicefakturaer
- Servicekreditnotaer
- Rentenotaer
- Purringer

## <a name="e-documents-in-sales"></a>E-dokumenter i salg

Hvis du vil opprette og sende en e-faktura til en kunde, må du opprette og bokføre salgsfakturaen. Hvis du vil lære mer om standardprosessen, kan du se [Fakturer salg](sales-how-invoice-sales.md).

Når du har bokført salgsdokumentet, åpner du siden **Bokført salgsfakturaer** for å komme til siden **E-dokumenter**.

### <a name="view-e-documents"></a>Vise e-dokumenter

Hvis du vil vise eksisterende e-dokumenter, gjør du følgende.

1. På siden **Bokført salgsfakturaer** velger du **E-dokument** og deretter **Åpne e-dokument**.
2. På siden **E-dokumenter** kan du vise grunnleggende informasjon om den bokførte fakturaen.
3. Feltet **Post** viser dokumentnummeret til det bokførte salgsfakturaen. Velg koblingen for å åpne dokumentet.
4. I feltet **Status for elektronisk dokument** kan du vise dokumentets sanntidsstatus og plasseringen i prosesspipelinen. Hvis dokumentet er bokført, er statusen **Behandlet**.

### <a name="e-document-statuses-and-logs"></a>E-dokumentstatuser og -logger

Hvis du vil ha mer informasjon om servicestatusnivået for e-dokumentet, kan du se hurtigfanen **Status for e-dokumenttjeneste**. På linjene viser systemet én eller flere tjenester som dokumentet har brukt. I det vanligste scenariet bruker hvert dokument bare én tjeneste. Et dokument kan imidlertid bruke flere tjenester.

- Kontroller feltet **E-dokumenttjenestekode** for å finne ut hvilken service som ble brukt.
- Kontroller feltet **E-dokumentstatus** for å finne gjeldende servicestatus for dette dokumentet.
- Hvis du vil ha mer informasjon, velger du feltet **Logger** for tjenesten på siden **E-dokumentlogger**. Det vises en kronologisk oversikt over de ulike statusene for dokumentet.
- Merk av for **Oppføringsnr.** og **Opprettet** og annen informasjon på siden **E-dokumentlogger**. I feltet **E-dokumentstatus** er den første statusen **Eksportert**, som angir at e-dokumentfilen er opprettet. Neste status er **Sendt**, som angir at dokumentet ble sendt til trykkeriet, hvis det er konfigurert.

Hvis du vil ha mer innsikt, velger du posten med statusen **Eksportert**, og deretter kjører du en av følgende handlinger:

- **Åpne tilordningslogger** – Få en oversikt over alle eksporterte felt fra kildetabellene i feltet **Opprinnelig verdi**. Hvis du brukte transformasjonsregler i eksportprosessen, kan du også få den endelige verdien i feltet **Ny verdi**.
- **Eksporter fil**- Eksporter XML-filen for manuell gjennomgang.

Hvis du vil vise kommunikasjonen mellom deg selv og tjenesten du sender dokumentet til, bruker du feltet **Kommunikasjonslogger**. Åpne siden **E-dokumentkommunikasjonslogger** for å vise detaljer om forespørselen og årsaksmeldingen med den tjenesten.

Hvis det er et problem med tjenesteleverandøren, og dokumentet ikke kan sendes, kan du se etter følgende indikatorer på siden **E-dokumenter**:

- Feltet **Status for elektronisk dokument** i hodet viser statusen **Feil**.
- Feltet **E-dokumentstatus** på hurtigfanen **Status for e-dokumenttjeneste** viser statusen for **Sendingsfeil**.
- Hurtigfanen **Feil og advarsler** inneholder én eller flere meldinger som oppgir årsaken til problemet.

Når problemet er løst, kjører du handlingene **Send dokument** manuelt. Hvis du trenger forskjellige handlinger, for eksempel **Gjenopprettet dokument**, **Kanseller dokument** eller **Få godkjenning**, kan du kjøre dem.

## <a name="overview-of-e-document-statuses"></a>Oversikt over e-dokumentstatuser

Hvis du vil ha en bedre oversikt over alle e-dokumenter i selskapet, kan du velge rollesenteret **Regnskapsfører** der det finnes e-dokumentstatuser. Der kan du finne e-dokumentaktiviteter som har følgende statuser:

- **Utgående e-dokumenter:**

    - Behandlet
    - Pågår
    - Feil


## <a name="see-also"></a>Se også

[Slik konfigurerer e-dokumenter i [!INCLUDE[prod_short](includes/prod_short.md)]](finance-how-setup-edocuments.md)    
[Slik bruker du e-dokumenter i kjøp](finance-how-use-edocuments-purchase.md)  
[Slik utvider du e-dokumenter i [!INCLUDE[prod_short](includes/prod_short.md)]](/dynamics365/business-central/dev-itpro/developer/devenv-extend-edocuments)    
[Økonomistyring](finance.md)    
[Fakturere salg](sales-how-invoice-sales.md)    
[Registrere kjøp med kjøpsfakturaer og ordrer](purchasing-how-record-purchases.md)    
[Arbeid med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
