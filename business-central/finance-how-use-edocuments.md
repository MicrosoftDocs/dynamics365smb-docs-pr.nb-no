---
title: Bruk e-dokumenter ved salg og kjøp
description: Lær hvordan du bruker funksjoner for e-dokumenter som er knyttet til salgs- og kjøpsfakturaer.
author: altotovi
ms.topic: conceptual
ms.devlang: al
ms.search.keywords: 'electronic document, electronic invoice, e-document, e-invoice, sales, purchase'
ms.search.form: '42, 43, 51, 6103, 6133, 6121, 9301, 9305, 9308'
ms.date: 10/03/2023
ms.author: altotovi
ms.service: dynamics-365-business-central
---

# <a name="use-e-documents-in-sales-and-purchases"></a>Bruk e-dokumenter ved salg og kjøp

Du kan bruke konfigurerte elektroniske dokumenter (e-dokumenter) med salgs- og kjøpsdokumenter.

Du kan bruke følgende dokumenter med e-dokumentfunksjonalitet:  

- Salg: 
    - Salgsfakturaer
    - Ordrer
    - Salgskreditnotaer
    - Servicefakturaer
    - Servicekreditnotaer
    - Rentenotaer
    - Purringer
- Kjøp: 
    - Kjøpsfakturaer
    - Bestillinger (bare opprett nytt dokument)
    - Kjøpskreditnotaer
    - Finanskladder

> [!NOTE]
> En bestilling kan for øyeblikket bare brukes når du oppretter dokumentet fra e-dokumentet fra leverandøren. Du kan imidlertid ikke oppdatere det eksisterende dokumentet med linjer du har fått fra leverandøren.  

## <a name="e-documents-in-sales"></a>E-dokumenter i salg

Hvis du vil opprette og sende en e-faktura til en kunde, må du opprette og bokføre salgsfakturaen. Hvis du vil lære mer om standardprosessen, kan du se [Fakturer salg](sales-how-invoice-sales.md).

Når du har bokført salgsdokumentet, åpner du siden **Bokført salgsfaktura** for å komme til siden **E-dokument** .

### <a name="view-e-documents"></a>Vise e-dokumenter

Hvis du vil vise eksisterende e-dokumenter, gjør du følgende.

1. På siden **Bokført salgsfaktura** velger du **E-dokument** \> **Åpne e-dokument**.
2. På siden **E-dokument** kan du vise grunnleggende informasjon om den bokførte fakturaen.
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

Hvis det er et problem med tjenesteleverandøren, og dokumentet ikke kan sendes, kan du se etter følgende indikatorer på siden **E-dokument**:

- Feltet **Status for elektronisk dokument** i hodet viser statusen **Feil**.
- Feltet **E-dokumentstatus** på hurtigfanen **Status for e-dokumenttjeneste** viser statusen for **Sendingsfeil**.
- Hurtigfanen **Feil og advarsler** inneholder én eller flere meldinger som oppgir årsaken til problemet.

Når problemet er løst, kjører du handlingene **Send dokument** manuelt. Hvis du trenger forskjellige handlinger, for eksempel **Gjenopprettet dokument**, **Kanseller dokument** eller **Få godkjenning**, kan du kjøre dem.

## <a name="e-documents-in-purchases"></a>E-dokumenter ved kjøp

Mottak av elektroniske fakturaer for kjøp i Dynamics 365 Business Central kan utføres som en kjørsel eller manuelt.

### <a name="run-the-batch-job"></a>Kjør kjørselen

> [!NOTE]
> Denne kjørselen er for automatisk innsamling av innkommende fakturaer. Den kan bare fungere i et land eller område der funksjonaliteten finnes.

Hver gang det kjøres en jobbkø, og den eksterne tjenesten har innkommende fakturaer som ble sendt fra leverandøren, samler systemet inn og importerer disse fakturaene. Følg disse trinnene for å fullføre prosessen.

1. Når kjørselen er ferdig, vises de nylig importerte fakturaene på siden **E-dokumenter** sammen med grunnleggende detaljinformasjon.
2. Hvis du vil vise flere detaljer, åpner du et bestemt e-dokument.
3. Hvis det ikke var noen feil eller problemer i e-dokumentet og tilordningen, viser feltet **Post** dokumentnummeret på kjøpsfakturaen som systemet opprettet automatisk. Velg koblingen for å åpne dokumentet. Dette systemopprettede dokumentet er ikke det bokførte dokumentet.
4. Hvis du vil gå direkte til kjøpsdokumentet, velger du **Post**-feltet. Når du har åpnet **Kjøpsfaktura**-siden, kontrollerer du dokumentet. Deretter, hvis alt er riktig, bokfør dokumentet.
5. Når du bokfører kjøpsdokumentet, oppdateres **Post**-feltet i **E-dokumentet** fra **Faktura** til **Kjøpsfaktura**, og nummeret på det bokførte kjøpsdokumentet er tilgjengelig. Du kan velge nummeret for å åpne den bokførte kjøpsfakturaen.

Detaljer om logger er de samme som i salgsprosessen for e-dokumenter.

Siden feil i salgsprosessen for det meste er knyttet til tilgjengeligheten til tjenesten, kan det inngående dokumentet inneholde flere årsaker. Den vanligste årsaken til en feil er at systemet ikke kan gjenkjenne linjene på e-dokumentet du fikk fra leverandøren. Derfor kan den ikke angi linjer i kjøpsfakturaen.

Det er to vanlige feil:

- Hvis du vil bruke denne bestemte linjen fra leverandørfakturaen som ble bokført direkte på finanskontoen, må du ha konfigurert verdien for **Tilordningstekst** riktig. For å omgå denne feilen hvis du vil bruke finanskonti, velger du **Tilordne tekst til konto** for å opprette en bestemt tilordning av verdien **Tilordningstekst** med verdien **Debetkontonummer** du vil bruke.
- Hvis du vil spore lagerbeholdningen og bruke linjer fra leverandørfakturaen til å fylle ut varer på dokumentlinjene, må du ha konfigurert **Varereferansenr** på riktig måte. For å unngå denne feilen, tilordner du det eksterne elementet med varenumrene ved hjelp av varereferanselisten. Se [Bruke varereferanser](inventory-how-use-item-cross-refs.md) for mer informasjon.

Når du har rettet feilene og advarslene, kan du angi manuelt når systemet skal opprette en kjøpsfaktura basert på oppsettet ditt ved å velge **Opprett dokument**.

### <a name="manually-import-invoices"></a>Importere fakturaer manuelt

Hvis du vil importere eksterne e-dokumenter manuelt, følger du denne fremgangsmåten.

1. Velg ikonet ![Lyspære som åpner funksjonen Fortell meg.](media/ui-search/search_small.png "Fortell hva du vil gjøre") og angi **E-dokumenttjeneste**, og velg deretter den relaterte koblingen.
2. Velg den aktive tjenesten på siden **E-dokumentservice**. 
3. Velg **Motta**, og last opp e-dokumentfilen du fikk fra leverandøren.
4. Hvis det oppstår en feilmelding, åpner du e-dokumentet for å løse problemene.
5. Når du er ferdig med å løse problemene, velger du **Opprett dokument** i gruppen **Importer manuelt**.
6. Når dokumentet er opprettet i Business Central, kan du vise det på samme måte som hvis du bruker en kjørsel.

## <a name="overview-of-e-document-statuses"></a>Oversikt over e-dokumentstatuser

Hvis du vil ha en bedre oversikt over alle e-dokumenter i selskapet, kan du velge rollesenteret **Regnskapsfører** der det finnes e-dokumentstatuser. Der kan du finne e-dokumentaktiviteter som har følgende statuser:

- **Utgående e-dokumenter:**

    - Behandlet
    - Pågår
    - Feil

- **Innkommende e-dokumenter:**

    - Behandlet
    - Pågår
    - Feil

## <a name="see-also"></a>Se også

[Konfigurere e-dokumenter i Business Central](finance-how-setup-edocuments.md)  
[Utvide e-dokumenter i Business Central](/dynamics365/business-central/dev-itpro/developer/devenv-extend-edocuments)  
[Økonomistyring](finance.md)  
[Fakturer salg](sales-how-invoice-sales.md)  
[Registrere kjøp med kjøpsfakturaer og ordrer](purchasing-how-record-purchases.md)  
[Arbeid med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)

[!INCLUDE[footer-include](includes/footer-banner.md)]
