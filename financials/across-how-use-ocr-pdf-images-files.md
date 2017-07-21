---
title: "Bruke OCR til å gjøre PDF om til e-fakturaer | Microsoft-dokumentasjon"
description: "Beskriver hvordan du kan bruke en OCR-tjeneste til å konvertere inngående PDF-filer til elektroniske dokumenter i Financials."
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: electronic document, e-invoice, incoming document, OCR, ecommerce, document exchange, import invoice
ms.date: 06/02/2017
ms.author: sgroespe
ms.translationtype: Human Translation
ms.sourcegitcommit: 81636fc2e661bd9b07c54da1cd5d0d27e30d01a2
ms.openlocfilehash: 020aeed82d6147641936dee2d7b860791c76d2ee
ms.contentlocale: nb-no
ms.lasthandoff: 07/07/2017


---
# <a name="how-to-use-ocr-to-turn-pdf-and-image-files-into-electronic-documents"></a>Bruke OCR til å konvertere PDF- og bildefiler til elektroniske dokumenter
Fra PDF- eller bildefiler som du mottar fra handelspartnere, kan du få en ekstern OCR-tjeneste (optisk tegngjenkjenning) til å generere elektroniske dokumenter som kan konverteres til dokumentposter i [!INCLUDE[d365fin](includes/d365fin_md.md)]. Når du for eksempel mottar en faktura i PDF-format fra leverandøren, kan du sende den til OCR-tjenesten fra vinduet **Inngående dokumenter**. Dette er beskrevet i første fremgangsmåte.

Som et alternativ til å sende filen fra vinduet **Inngående dokumenter** kan du sende filen til OCR-tjenesten via e-post. Deretter, når du får tilbake det elektroniske dokumentet, opprettes det automatisk en relatert innkommende dokumentpost. Dette er beskrevet i andre fremgangsmåte.

Etter noen sekunder vil du motta filen tilbake fra OCR-tjenesten som en elektronisk faktura som kan konverteres til en kjøpsfaktura for leverandøren. Dette er beskrevet i tredje fremgangsmåte.

Siden OCR er basert på optisk gjenkjenning, er det sannsynlig at OCR-tjenesten vil tolke tegn i PDF-filer eller bildefiler feilaktig når den først behandleren en bestemt leverandørs dokumenter. Det kan hende at den ikke tolker firmalogoen som leverandørnavn, eller det kan hende at den feiltolker det totale beløpet på en kvittering på grunn av oppsettet. Hvis du vil unngå disse feilene fremover, kan du rette opp feilene i en egen versjon av vinduet **Inngående dokument**. Du kan deretter sende rettelser tilbake til OCR-tjenesten for å lære den å tolke bestemte tegn på rett måte neste gang den behandler et PDF- eller bildedokument for den samme leverandøren. Hvis du vil ha mer informasjon, kan du se avsnittet "Lære opp OCR-tjenesten for å unngå feil".

Trafikken av filer til og fra OCR-tjenesten behandles av en dedikerte jobbkøpost, som opprettes automatisk når du aktiverer den relaterte tjenestetilkoblingen. Hvis du vil ha mer informasjon, kan du se [Konfigurere inngående dokumenter](across-how-setup-income-documents.md).

## <a name="to-send-a-pdf-or-image-file-to-the-ocr-service-from-the-incoming-documents-window"></a>Sende en PDF- eller bildefil til OCR-tjenesten fra vinduet **Inngående dokumenter**
1. Velg ikonet ![Søk etter side eller rapport](media/ui-search/search_small.png "Ikonet Søk etter side eller rapport"), angi **Inngående dokumenter**, og velg deretter den relaterte koblingen.
2. Opprett en ny innkommende dokumentpost, og legg ved filen. Hvis du vil ha mer informasjon, kan du se [Opprette innkommende dokumentposter](across-how-create-income-document-records.md).  
3. I vinduet **Innkommende** dokumenter velger du én eller flere linjer, og deretter velger du handlingen **Send til jobbkø**.

    Verdien i **OCR-stauts**-feltet endres til **Klar**. Den vedlagte PDF- eller bildefilen sendes til OCR-tjenesten av jobbkøen i henhold til tidsplanen, forutsatt at det ikke finnes feil.
4. I vinduet **Inngående dokumenter** velger du én eller flere linjer, og deretter velger du handlingen **Send til OCR-tjeneste**.

Verdien i **OCR-status**-feltet endres til **Sendt**, forutsatt at det ikke finnes noen feil.

## <a name="to-send-a-pdf-or-image-file-to-the-ocr-service-by-email"></a>Sende en PDF- eller bildefil til OCR-tjenesten via e-post
Fra e-postprogrammet kan du sende en e-post til leverandøren av OCR-tjenesten med PDF- eller bildefilen vedlagt. Du finner informasjon om e-postadressen du skal sende til, på nettstedet for OCR-tjenesteleverandøren.

Fordi det ikke finnes noen inngående dokumentoppføring for filen, opprettes en ny post automatisk i vinduet **Inngående dokumenter** når du mottar det resulterende elektroniske dokumentet fra OCR-tjenesten. Hvis du vil ha mer informasjon, kan du se [Opprette innkommende dokumentposter](across-how-create-income-document-records.md).

> [!NOTE]  
>   Hvis du arbeider på et nettbrett eller en telefon, kan du sende filen til OCR-tjenesten så snart du har tatt et bilde av dokumentet, eller du kan opprette et innkommende dokument direkte. Hvis du vil ha mer informasjon, kan du se avsnittet "Opprette innkommende dokumentposter ved å ta et bilde" i [Opprette innkommende dokumentposter](across-how-create-income-document-records.md).

## <a name="to-receive-the-resulting-electronic-document-from-the-ocr-service"></a>Slik mottar du det resulterende elektroniske dokumentet fra OCR-tjenesten:
Det elektroniske dokumentet som opprettes av OCR-tjenesten fra PDF- eller bildefilen, mottas automatisk inn i vinduet **Inngående dokumenter** via jobbkøposten som settes opp når du aktiverer OCR-tjenesten.

Hvis du ikke bruker en jobbkø, eller hvis du vil motta et ferdig OCR-dokument raskere enn per jobbkøplanen, kan du velge **Motta fra OCR-tjeneste**-knappen. Dette vil hente alle dokumenter som er fullført av OCR-tjenesten.

> [!NOTE]  
>   Hvis OCR-tjenesten er konfigurert til å kreve manuell godkjenning av behandlede dokumenter, vil feltet **OCR-status** inneholde **Venter på bekreftelse**. I så fall gjør du følgende for å logge deg på webområdet til OCR-tjenesten og bekrefte et OCR-dokument manuelt.

1. I **OCR-status**-feltet velger du hyperkoblingen **Venter på bekreftelse**. Eller velg flisen **Venter på bekreftelse** på Hjem-siden.
2. Logg på med legitimasjonen for OCR-tjenestekontoen på webområdet for OCR-tjenesten. Dette er legitimasjonen du også brukte da du satte opp tjenesten. Hvis du vil ha mer informasjon, kan du se delen "Slik definerer du en OCR-tjeneste" i [Konfigurere inngående dokumenter](across-how-setup-income-documents.md).

    Hvis du åpner webområdet fra **OCR-status**-feltet, vises det aktuelle dokumentet umiddelbart etter påloggingen. Hvis du åpner webområdet ved å velge flisen på hjemmesiden, på den første OCR-siden som åpnes, må du velge **Start**-knappen på **Bekreft**-fanen eller dobbeltklikke dokumentet som du vil bekrefte.

    Informasjon for OCR-dokumentet vises, med både kildeinnholdet i PDF-filen eller bildefilen og de resulterende OCR-feltverdiene.
3. Gå gjennom de ulike feltverdiene og rediger manuelt eller angi verdier i felt som OCR-tjenesten har merket som usikre.
4. Velg **OK**. OCR-prosessen er fullført, og det resulterende elektroniske dokumentet sendes til **Inngående dokumenter**-vinduet i [!INCLUDE[d365fin](includes/d365fin_md.md)] i henhold til jobbkøplanen.

    Hvis du åpner webområdet ved å velge flisen på hjemmesiden, vises automatisk andre OCR-dokumenter som skal bekreftes, på webområdet.
5. Gjenta trinn 4 for andre OCR-dokumenter som skal bekreftes.

Nå kan du fortsette å opprette dokumentposter for de elektroniske dokumentene som er mottatt i [!INCLUDE[d365fin](includes/d365fin_md.md)], manuelt eller automatisk. Hvis du vil ha mer informasjon, kan du se neste fremgangsmåte. Du kan også koble den nye innkommende dokumentposten til eksisterende postert eller ikke-postert dokument slik at kildefilen er lett tilgjengelige fra [!INCLUDE[d365fin](includes/d365fin_md.md)]. Hvis du vil ha mer informasjon, kan du se [Behandle inngående dokumenter](across-process-income-documents.md).

## <a name="to-create-a-purchase-invoice-from-an-electronic-document-received-from-the-ocr-service"></a>Slik oppretter du en kjøpsfaktura fra et elektronisk dokument som er mottatt fra OCR-tjenesten:
Følgende fremgangsmåte beskriver hvordan du oppretter en post for kjøpsfaktura fra en leverandørfaktura mottatt som et elektronisk dokument fra OCR-tjenesten. Fremgangsmåten er den samme når du oppretter for eksempel en finanskladdelinje fra en utgiftskvittering.

> [!NOTE]  
>   Feltene **Beskrivelse** og **Nr.** på dokumentlinjene som er opprettet, fylles bare ut hvis du først har tilordnet teksten som finnes på OCR-dokumentet til de to feltene i [!INCLUDE[d365fin](includes/d365fin_md.md)]. Du kan gjøre dette enten som varekryssreferanser, for dokumentlinjer av typen Vare, eller som tekst-til-konto-tilordninger, for bilag eller kladdelinjer av typen Finanskonto. Hvis du vil ha mer informasjon, kan du se verktøytipset for **Kryssreferanser**-handlingen på varekortene og den relaterte fremgangsmåten [Tilordne tekst på gjentakende betalinger til kontoer for automatisk avstemming](receivables-how-map-text-recurring-payments-accounts-auto-reconcilliation.md).

For innkommende dokumenter bruker du vanligvis handlingen **Tilordne tekst til konto** for å definere at en bestemt tekst på en leverandørfaktura som er mottatt fra OCR-tjenesten, tilordnes til en bestemt leverandørkonto. Deler av beskrivelsen av det innkommende dokumentet som finnes som tilordningstekst, betyr at **Nr.**-feltet på det resulterende bilaget eller kladdelinjene av typen Finanskonto, fylles deretter ut med den aktuelle leverandøren.

I tillegg til å tilordne til en leverandørkonto eller finanskontoer, kan du også tilordne til en bankkonto. Dette er praktisk, for eksempel for elektroniske dokumenter for utgifter som allerede er betalt, der du vil opprette en finanskladdelinje som er klar til å bokføre på en bankkonto.

1. Velg linjen for inngående dokument for det elektroniske leverandørdokumentet som er mottatt fra OCR-tjenesten.
2. Hvis du vil tilordne tekst på dokumentet til leverandørens konto, en debetkonto, kan du velge handlingen **Tilordne tekst til konto** og fylle ut **Tekst-til-konto-tilordning**-vinduet med opplysninger som gjelder for leverandøren fra nå av. Hvis du vil ha mer informasjon, kan du se [Tilordne tekst på gjentakende betalinger til kontoer for automatisk avstemming](receivables-how-map-text-recurring-payments-accounts-auto-reconcilliation.md)
3. Hvis du vil tilordne varenumrene i dokumentet til beskrivelsene av leverandørens varer, åpner du kortet for hver vare, og velger deretter handlingen **Kryssreferanser** for å definere kryssreferanser mellom varebeskrivelsene dine og dem til leverandøren.
4. I vinduet **Inngående dokumenter** velger du handlingen **Opprett dokument**.

Det blir opprettet en kjøpsfaktura i [!INCLUDE[d365fin](includes/d365fin_md.md)] basert på informasjonen i det elektroniske leverandørdokumentet som du mottok fra OCR-tjenesten.

Eventuelle valideringsfeil, vanligvis knyttet til feil eller manglende hoveddata i [!INCLUDE[d365fin](includes/d365fin_md.md)], vises i **Feil og advarsler**-hurtigfanen. Hvis du vil ha mer informasjon, kan du se "Håndtere feil ved mottak av elektroniske dokumenter".

## <a name="to-handle-errors-when-receiving-electronic-documents"></a>Håndtere feil ved mottak av elektroniske dokumenter
1. Velg linjen for et elektronisk dokumentet som er mottatt fra OCR-tjenesten med feil, i vinduet **Inngående dokumenter**. Dette angis av en feilverdi i **OCR-status**-feltet.
2. Velg handlingen **Rediger** for å åpne **Inngående dokumenter**-vinduet.
3. På **Feil og advarsler**-hurtigfanen merker du meldingen og velger **Åpne relatert post**.
4. Vinduet som inneholder feil eller manglende data, for eksempel et leverandørkort med en manglende feltverdi, åpnes.
5. Rett opp feilen eller feilene som beskrevet i hver feilmelding.
6. Fortsett med å behandle det innkommende elektroniske dokumentet ved å velge **Opprett manuelt** på nytt.
7. Gjenta trinn 5 og 6 for eventuelle gjenværende feil til det elektroniske dokumentet kan mottas.

## <a name="to-train-the-ocr-service-to-avoid-errors"></a>Lære opp OCR-tjenesten for å unngå feil
Siden OCR er basert på optisk gjenkjenning, er det sannsynlig at OCR-tjenesten kan tolke tegn i PDF-filer eller bildefiler feilaktig når den først behandler dokumenter fra for eksempel en bestemt leverandør. Det kan hende at den ikke tolker firmalogoen som leverandørnavn, eller det kan hende at den feiltolker det totale beløpet på en utgiftskvittering på grunn av oppsettet. Du kan rette data fra OCR-tjenesten for å unngå slike feil senere, og deretter sende tilbakemeldingen til tjenesten.

Vinduet **OCR-datakorrigering**, som du åpner fra vinduet **Inngående dokumenter**, viser feltene fra hurtigfanen **Økonomisk informasjon** i to kolonner, én med OCR-data du kan redigere, og én med skrivebeskyttede OCR-data. Når du velger **Send OCR-tilbakemelding**, sendes innholdet i vinduet **OCR-datakorrigering** til OCR-tjenesten. Neste gang tjenesten behandler PDF-filer eller bildefiler som inneholder de aktuelle dataene, blir korrigeringene dine tatt med for å unngå de samme feilene.

1. Velg ikonet ![Søk etter side eller rapport](media/ui-search/search_small.png "Ikonet Søk etter side eller rapport"), angi **Inngående dokumenter**, og velg deretter den relaterte koblingen.
2. Åpne en innkommende dokumentpost som inneholder data som mottas fra OCR-tjenesten som du vil korrigere.
3. I vinduet **Inngående dokument** velger du handlingen **Korriger OCR-Data**.
4. I vinduet **OCR-datakorrigering** overskriver du dataene i den redigerbare kolonnen for hvert felt som har feil verdi.
5. Hvis du vil angre korrigeringer du har gjort etter at du åpnet vinduet **OCR-datakorrigering**, velger du handlingen **Tilbakestill OCR-data**.
6. Hvis du vil sende korrigeringer til OCR-tjenesten, velger du handlingen **Send OCR-tilbakemelding**.
7. Hvis du vil lagre rettelsene, lukker du vinduet **OCR-datakorrigering**.

Feltene i hurtigfanen **Økonomisk informasjon** i vinduet **Inngående dokumenter**, oppdateres med nye verdier du angav i trinn 4.

## <a name="see-also"></a>Se også
[Behandle inngående dokumenter](across-process-income-documents.md)  
[Inngående dokumenter](across-income-documents.md)  
[Innkjøp](purchasing-manage-purchasing.md)  
[Arbeide med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

