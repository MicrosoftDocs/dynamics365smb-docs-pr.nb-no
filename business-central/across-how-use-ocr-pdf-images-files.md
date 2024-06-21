---
title: Bruk OCR til å gjøre PDF om til e-fakturaer
description: Beskriver hvordan du kan bruke en OCR-tjeneste til å konvertere inngående PDF-filer til elektroniske dokumenter.
documentationcenter: ''
author: brentholtorf
ms.topic: conceptual
ms.devlang: al
ms.search.keywords: 'electronic document, e-invoice, incoming document, OCR, ecommerce, document exchange, import invoice'
ms.date: 06/14/2022
ms.author: bholtorf
ms.service: dynamics-365-business-central
ms.reviewer: bholtorf
---
# <a name="use-ocr-to-turn-pdf-and-image-files-into-electronic-documents"></a>Bruke OCR til å konvertere PDF- og bildefiler til elektroniske dokumenter

Fra PDF- eller bildefiler som du mottar fra handelspartnere, kan du få en ekstern OCR-tjeneste (optisk tegngjenkjenning) til å generere elektroniske dokumenter som kan konverteres til dokumentposter i [!INCLUDE[prod_short](includes/prod_short.md)]. Når du for eksempel mottar en faktura i PDF-format fra leverandøren, kan du [sende den til OCR-tjenesten fra siden **Innkommende dokumenter**](#to-send-a-pdf-or-image-file-to-the-ocr-service-from-the-incoming-documents-page).

Som et alternativ til å sende filen fra siden **Inngående dokumenter** kan OCR-tjenesten tilby alternativet om å [behandle filene videresendt til en egen e-postadresse](#to-send-a-pdf-or-image-file-to-the-ocr-service-by-email). Deretter, når du får tilbake det elektroniske dokumentet, opprettes det automatisk en relatert innkommende dokumentpost i [!INCLUDE[prod_short](includes/prod_short.md)].

Etter noen sekunder sender OCR-tjenesten den behandlede filen til siden for **innkommende dokumenter** som en elektronisk dokumentpost som kan [konverteres til en kjøpsfaktura for leverandøren](#to-receive-the-resulting-electronic-document-from-the-ocr-service), en salgsfaktura, en kreditnota eller en kladdepost.

Siden OCR er basert på optisk gjenkjenning, er det sannsynlig at OCR-tjenesten vil tolke tegn i PDF-filer eller bildefiler feilaktig når den først behandleren en bestemt leverandørs dokumenter. Det kan hende at den ikke tolker firmalogoen som leverandørnavn, eller det kan hende at den feiltolker det totale beløpet på en kvittering på grunn av oppsettet. Hvis du vil unngå disse feilene fremover, kan du rette opp feilene i en egen versjon av siden **Inngående dokument**. Du kan deretter sende rettelser tilbake til OCR-tjenesten for å lære den å tolke bestemte tegn og felter på rett måte neste gang den behandler et PDF- eller bildedokument for den samme leverandøren. Hvis du vil ha mer informasjon, kan du se [Lær opp OCR-tjenesten for å unngå feil](across-how-use-ocr-pdf-images-files.md#to-train-the-ocr-service-to-avoid-errors).

Trafikken av filer til og fra OCR-tjenesten behandles av en egen jobbkøpost. Denne jobbkøen opprettes automatisk når du aktiverer den eksterne OCR-tjenestetilkoblingen. Hvis du vil ha mer informasjon, kan du se [Konfigurer innkommende dokumenter](across-how-setup-income-documents.md).

> [!NOTE]
> OCR-funksjonen tilbys av eksterne leverandører. Velg en tjenestepakke som passer for organisasjonen eller landet/området. Finn tjenester som er kompatible med [!INCLUDE[prod_short](includes/prod_short.md)] og detaljer om tilgjengelige funksjoner ved [AppSource.microsoft.com](https://go.microsoft.com/fwlink/?linkid=2081646).

## <a name="to-send-a-pdf-or-image-file-to-the-ocr-service-from-the-incoming-documents-page"></a>Send en PDF- eller bildefil til OCR-tjenesten fra siden Innkommende dokumenter

1. Velg ikonet ![Lyspære som åpner funksjonen Fortell meg.](media/ui-search/search_small.png "Fortell hva du vil gjøre") , angi **Innkommende dokumenter**, og velg deretter den relaterte koblingen.
2. Opprett en ny innkommende dokumentpost, og legg ved filen. Hvis du vil ha mer informasjon, kan du se [Opprette innkommende dokumentposter](across-how-create-income-document-records.md).  
3. På siden **Innkommende dokumenter** velger du én eller flere linjer, og deretter velger du handlingen **Send til jobbkø**.

   Verdien i **OCR-stauts**-feltet endres til **Klar**. Den vedlagte PDF- eller bildefilen sendes til OCR-tjenesten av jobbkøen i henhold til tidsplanen, hvis det ikke finnes feil.
4. På siden **Inngående dokumenter** velger du én eller flere linjer, og deretter velger du handlingen **Send til OCR-tjeneste** for å sende filene til behandling umiddelbart.

   Verdien i **OCR-status**-feltet endres til **Sendt**, hvis det ikke finnes noen feil.

## <a name="to-send-a-pdf-or-image-file-to-the-ocr-service-by-email"></a>Sende en PDF- eller bildefil til OCR-tjenesten via e-post

Fra e-postprogrammet kan du videresende en e-post til leverandøren av OCR-tjenesten med PDF- eller bildefilen vedlagt. Du finner informasjon om e-postadressen du skal sende til, på nettstedet for OCR-tjenesteleverandøren.

Fordi det ikke finnes noen innkommende dokumentoppføring for filen, opprettes en ny post automatisk på siden **Innkommende dokumenter** når OCR-tjenesten sender det resulterende elektroniske dokumentet. Hvis du vil ha mer informasjon, kan du se [Opprett innkommende dokumentposter](across-how-create-income-document-records.md).

> [!NOTE]  
> Hvis du arbeider på et nettbrett eller en telefon, kan du sende filen til OCR-tjenesten så snart du har tatt et bilde av dokumentet, eller du kan opprette et innkommende dokument direkte. Hvis du vil ha mer informasjon, kan du se [Opprett en innkommende dokumentpost ved å ta et bilde](across-how-create-income-document-records.md#create-an-incoming-document-record-by-taking-a-photo).

## <a name="to-receive-the-resulting-electronic-document-from-the-ocr-service"></a>Slik mottar du det resulterende elektroniske dokumentet fra OCR-tjenesten

Det elektroniske dokumentet som opprettes av OCR-tjenesten fra PDF- eller bildefilen, mottas automatisk inn på siden **Inngående dokumenter** via jobbkøposten som settes opp når du aktiverer OCR-tjenesten.

Hvis du ikke bruker en jobbkø, eller hvis du vil motta et ferdig OCR-dokument raskere enn per jobbkøplanen, kan du velge **Motta fra OCR-tjeneste**-handlingen. Dette alternativet henter alle dokumenter som er fullført av OCR-tjenesten.

> [!NOTE]  
> Hvis OCR-tjenesten er konfigurert til å kreve manuell godkjenning av behandlede dokumenter, vil feltet **OCR-status** inneholde **Venter på bekreftelse**. I så fall gjør du følgende for å logge deg på nettstedet til OCR-tjenesten og bekrefte et OCR-dokument manuelt.

1. I **OCR-status**-feltet velger du hyperkoblingen **Venter på bekreftelse**.
2. Logg på med legitimasjonen for OCR-tjenestekontoen på nettstedet for OCR-tjenesten. Hvis du vil ha mer informasjon, kan du se [Definer en OCR-tjeneste](across-how-setup-income-documents.md#to-set-up-an-ocr-service).

   Informasjon for OCR-dokumentet vises, med både kildeinnholdet i PDF-filen eller bildefilen og de resulterende OCR-feltverdiene.
3. Gå gjennom feltverdiene og rediger manuelt eller angi verdier i felter som OCR-tjenesten har merket som usikre.
4. Velg **OK**. OCR-prosessen er fullført, og det resulterende elektroniske dokumentet sendes til **Innkommende dokumenter**-siden i [!INCLUDE[prod_short](includes/prod_short.md)] i henhold til jobbkøplanen.
5. Gjenta trinn 2 til 4 for andre OCR-dokumenter som skal bekreftes.

Nå kan du fortsette å opprette dokumentposter for de elektroniske dokumentene som er mottatt i [!INCLUDE[prod_short](includes/prod_short.md)], manuelt eller automatisk. Hvis du vil ha mer informasjon, kan du se neste fremgangsmåte. Du kan også [koble den nye innkommende dokumentposten til eksisterende posterte eller ikke-posterte dokumenter](across-how-connect-disconnect-income-document-records.md) slik at kildefilen er lett tilgjengelige fra [!INCLUDE[prod_short](includes/prod_short.md)].

## <a name="to-create-a-purchase-invoice-from-an-electronic-document-received-from-the-ocr-service"></a>Slik oppretter du en kjøpsfaktura fra et elektronisk dokument som er mottatt fra OCR-tjenesten:

Følgende fremgangsmåte beskriver hvordan du oppretter en post for kjøpsfaktura fra en leverandørfaktura mottatt som et elektronisk dokument fra OCR-tjenesten. Fremgangsmåten er den samme når du oppretter for eksempel en finanskladdelinje fra en utgiftskvittering., eller en ordreretur fra en kunde.

> [!NOTE]  
> Feltene **Beskrivelse** og **Nr.** på dokumentlinjene som er opprettet, fylles bare ut hvis du først har tilordnet teksten som finnes på OCR-dokumentet til de to feltene i [!INCLUDE[prod_short](includes/prod_short.md)]. Du kan utføre denne tilordningen som varereferanser, for dokumentlinjer av typen Vare. Se [Bruke varereferanser](inventory-how-use-item-cross-refs.md) for mer informasjon. Du kan også bruke funksjonen **Tekst-til-konto-tildeling**. Hvis du vil ha mer informasjon, kan du se delen [Tildel tekst i et innkommende dokument til en bestemt leverandør, finanskonto eller bankkonto](across-how-use-ocr-pdf-images-files.md#to-map-text-on-an-incoming-document-to-a-specific-vendor-account).

1. Merk linjen for det inngående dokumentet, og velg deretter **Opprett dokument**-handlingen.

Det blir opprettet en kjøpsfaktura i [!INCLUDE[prod_short](includes/prod_short.md)] basert på informasjonen i det elektroniske leverandørdokumentet som du mottok fra OCR-tjenesten. Informasjon settes inn i den nye kjøpsfakturaen basert på tildelingen du har definert som referanse eller som tekst-til-konto-tildeling.

Eventuelle valideringsfeil, vanligvis knyttet til feil eller manglende data i [!INCLUDE[prod_short](includes/prod_short.md)], vises i **Feil og advarsler**-hurtigfanen. Hvis du vil ha mer informasjon, kan du se [Håndter feil ved mottak av elektroniske dokumenter](across-how-use-ocr-pdf-images-files.md#to-handle-errors-when-receiving-electronic-documents).

### <a name="to-map-text-on-an-incoming-document-to-a-specific-vendor-account"></a>Slik tilordner du tekst i et inngående dokument til en bestemt leverandørkonto:

For innkommende dokumenter bruker du vanligvis handlingen **Tilordne tekst til konto** for å definere at en bestemt tekst på en leverandørfaktura som er mottatt fra OCR-tjenesten, tilordnes til en bestemt leverandørkonto. Hvis du videresender en del av det innkommende dokumentbeskrivelsen som finnes som en tildelingstekst, betyr dette at feltet **Leverandørnr.** i resulterende dokument- eller kladdelinjer av typen *finanskonto* fylles ut med den aktuelle leverandøren.

I tillegg til å tilordne til en leverandørkonto eller finanskontoer, kan du også tildele tekst til en bankkonto. Dette alternativet er nytt for eksempel for elektroniske dokumenter for utgifter som allerede er betalt, der du vil opprette en finanskladdelinje som er klar til å bokføre på en bankkonto.

1. Velg den aktuelle inngående dokumentlinjen, og velg deretter **Tilordne tekst til konto**-handlingen. Siden **Tekst-til-konto-tilordning** åpnes.
2. I feltet **Tilordningstekst** angir du en hvilken som helst tekst som vises på leverandørfakturaer som du vil opprette kjøpsdokumenter eller kladdelinjer for. Du kan angi opptil 50 tegn.
3. I feltet **Leverandørnummer** angir du leverandøren som det resulterende kjøpsdokumentet eller kladdelinjen blir opprettet for.
4. I feltet **Debetkontonummer** angir du finanskontoen for debettype som skal settes inn på det resulterende kjøpsbilaget eller kladdelinjen av typen Finanskonto.
5. I feltet **Kreditkontonummer** angir du finanskontoen for kredittype som skal settes inn på det resulterende kjøpsbilaget eller kladdelinjen av typen Finanskonto.

   > [!NOTE]
   > Ikke bruk **Saldokildetype**- og **Saldokildenummer**-feltet i forbindelse med inngående dokumenter. De brukes bare til automatisk betalingsavstemming. Hvis du vil ha mer informasjon, kan du se [Tilordne tekst på gjentakende betalinger til kontoer for automatisk avstemming](receivables-how-map-text-recurring-payments-accounts-auto-reconcilliation.md)
6. Gjenta trinn 2 til 5 for all tekst i inngående dokumenter som du vil opprette dokumenter automatisk for.

## <a name="to-handle-errors-when-receiving-electronic-documents"></a>Håndtere feil ved mottak av elektroniske dokumenter

1. Velg linjen for et elektronisk dokumentet som er mottatt fra OCR-tjenesten med feil, på siden **Innkommende dokumenter**, angitt av *feilverdien* i feltet **OCR-status**.
2. Velg handlingen **Rediger** for å åpne **Inngående dokumenter**-siden.
3. På **Feil og advarsler**-hurtigfanen merker du meldingen og velger **Åpne relatert post**.
4. Siden som inneholder feil eller manglende data, for eksempel et leverandørkort med en manglende feltverdi, åpnes.
5. Rett opp feilen eller feilene som beskrevet i hver feilmelding.
6. Fortsett med å behandle det innkommende elektroniske dokumentet ved å velge **Opprett manuelt** på nytt.
7. Gjenta trinn 5 og 6 for eventuelle gjenværende feil til det elektroniske dokumentet kan mottas.

## <a name="to-train-the-ocr-service-to-avoid-errors"></a>Lære opp OCR-tjenesten for å unngå feil

Siden OCR er basert på optisk gjenkjenning, kan OCR-tjenesten feilaktig tolke tegn i PDF-filer eller bildefiler når den først behandler dokumenter fra for eksempel en bestemt leverandør. Det kan hende at den ikke tolker firmalogoen som leverandørnavn, eller det kan hende at den feiltolker det totale beløpet på en utgiftskvittering på grunn av oppsettet. Du kan rette data fra OCR-tjenesten for å unngå slike feil senere, og deretter sende tilbakemeldingen til tjenesten.

Siden **OCR-datakorrigering**, som du åpner fra siden **Inngående dokumenter**, viser feltene fra hurtigfanen **Økonomisk informasjon** i to kolonner, én med OCR-data du kan redigere, og én med skrivebeskyttede OCR-data. Når du velger **Send OCR-tilbakemelding**, sendes innholdet på siden **OCR-datakorrigering** til OCR-tjenesten. Neste gang tjenesten behandler PDF-filer eller bildefiler som inneholder de aktuelle dataene, blir korrigeringene dine tatt med for å forbedre dokumentgjenkjenning.

1. Velg ikonet ![Lyspære som åpner funksjonen Fortell meg.](media/ui-search/search_small.png "Fortell hva du vil gjøre") , angi **Innkommende dokumenter**, og velg deretter den relaterte koblingen.
2. Åpne en innkommende dokumentpost som inneholder data som mottas fra OCR-tjenesten som du vil korrigere.
3. På siden **Inngående dokument** velger du handlingen **Korriger OCR-Data**.
4. På siden **OCR-datakorrigering** overskriver du dataene i den redigerbare kolonnen for hvert felt som har feil verdi.
5. Hvis du vil angre korrigeringer du har gjort etter at du åpnet siden **OCR-datakorrigering**, velger du handlingen **Tilbakestill OCR-data**.
6. Hvis du vil sende korrigeringer til OCR-tjenesten, velger du handlingen **Send OCR-tilbakemelding**.
7. Hvis du vil lagre rettelsene, lukker du siden **OCR-datakorrigering**.

Feltene i hurtigfanen **Økonomisk informasjon** på siden **Inngående dokumenter**, oppdateres med nye verdier du angav i trinn 4.

## <a name="see-also"></a>Se også

[Opprett innkommende dokumentposter](across-how-create-income-document-records.md)
[Opprett innkommende dokumentposter direkte fra dokumenter og enheter](across-how-connect-disconnect-income-document-records.md)
[Innkommende dokumenter](across-income-documents.md)  
[Innkjøp](purchasing-manage-purchasing.md)  
[Arbeid med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
