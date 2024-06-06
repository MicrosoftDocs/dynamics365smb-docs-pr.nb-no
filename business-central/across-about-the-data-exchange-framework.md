---
title: Om rammeverket for datautveksling
description: Denne artikkelen forklarer hvordan du bruker rammeverket for datautveksling til å håndtere utvekslingen av data i forretningsdokumenter som fakturaer med forretningspartnere.
author: brentholtorf
ms.topic: conceptual
ms.devlang: al
ms.search.keywords: 'Data exchange framework, data files, data exchange, electronic document, invoice, Business Central, business document, standard-compliant file, OCR'
ms.search.form: '189,'
ms.date: 12/13/2023
ms.author: bholtorf
ms.service: dynamics-365-business-central
---
# Rammeverket for datautveksling

Du kan bruke rammeverket for datautveksling til å utveksle forretningsdokumenter, bankfiler, valutakurser og andre datafiler med forretningspartnerne eller myndigheter.

Som administrator eller Microsoft-partner kan du bruke rammeverket i nye integrasjonsfunksjoner ved å definere hvilke data som skal utveksles, og hvordan. Filformater for utveksling av data i bankfiler, elektroniske dokumenter, valutakurser og andre med ERP-systemer varierer for eksempel avhengig av leverandøren av datafilen eller -strømmen og landet/regionen. [!INCLUDE[prod_short](includes/prod_short.md)] støtter ulike bankfilformater og dataservicestandarder. Hvis du vil ha støtte for andre elektroniske dokumentformater, kan du bruke rammeverket for datautveksling.

 Diagrammene nedenfor viser arkitekturen til rammeverket for datautveksling.  

 ![Rammeverket for datautveksling &#45; Import.](media/across-data-exchange/dataexchangeframework_import.png)  

 ![Rammeverket for datautveksling &#45; Eksport.](media/across-data-exchange/dataexchangeframework_export.png)  

## Elektroniske dokumenter

Som et alternativ til å sende forretningsdokumenter som filvedlegg via e-post, kan du sende og motta dem elektronisk. Et elektronisk dokument er en standardkompatibel fil som representerer et forretningsdokument, for eksempel en faktura fra en leverandør som du kan motta og konvertere til en kjøpsfaktura i [!INCLUDE[prod_short](includes/prod_short.md)]. Handelspartnere utveksler elektroniske dokumenter gjennom eksterne dokumentutvekslingstjenester. Som standard støtter [!INCLUDE[prod_short](includes/prod_short.md)] sending og mottak av elektroniske fakturaer og kreditnotaer i PEPPOL-format, som støttes av de største leverandørene av dokumentutvekslingstjenester. En større leverandør av dokumentutvekslingstjenester, Tradeshift, er forhåndskonfigurert og klar til å bli definert for firmaet. Hvis du vil ha støtte for andre elektroniske dokumentformater, må du opprette nye datautvekslingsdefinisjoner.  

Fra PDF- eller bildefiler som representerer inngående dokumenter, kan du få en ekstern OCR-tjeneste (optisk tegngjenkjenning) til å opprette elektroniske dokumenter som du deretter kan konvertere til dokumentposter i [!INCLUDE[prod_short](includes/prod_short.md)], på samme måte som for elektroniske PEPPOL-dokumenter. Når du for eksempel mottar en faktura i PDF-format fra leverandøren, kan du sende den til OCR-tjenesten fra siden **Inngående dokumenter**. Etter noen få sekunder får du filen tilbake som en elektronisk faktura som kan konverteres til en kjøpsfaktura for leverandøren. Hvis du sender filen til OCR-tjenesten via e-post, opprettes deretter en ny post for inngående dokument automatisk når du får det elektroniske dokumentet tilbake.  

Hvis du for eksempel vil sende en salgsfaktura som et elektronisk PEPPOL-dokument, velger du alternativet **Elektronisk dokument** i dialogboksen **Bokfør og send**. Herfra kan du også angi kundens standardprofil for dokumentsending. Først må du definere forskjellige hoveddata, for eksempel firmainformasjon, kunder, varer og enheter. Disse brukes til å identifisere forretningspartnere og elementer når du konverterer data i feltene i [!INCLUDE[prod_short](includes/prod_short.md)] til elementene i den utgående dokumentfilen. Datakonverteringen og sendingen av PEPPOL-salgsfakturaen blir utført av dedikerte kodeenheter og XML-porter, representert av det elektronisk dokumentformatet **PEPPOL**.  

Hvis du for eksempel vil motta en faktura fra en leverandør som et elektronisk PEPPOL-dokument, kan du behandle dokumentet på siden **Innkommende dokumenter** for å konvertere det til en kjøpsfaktura i [!INCLUDE[prod_short](includes/prod_short.md)]. Du kan angi jobbkøfunksjonen til å behandle slike filer med jevne mellomrom, eller du kan starte prosessen manuelt. Først må du definere forskjellige hoveddata, for eksempel firmainformasjon, leverandører, varer og enheter. Disse brukes til å identifisere forretningspartnere og elementer når du konverterer data i elementer i den innkommende dokumentfilen til felt i [!INCLUDE[prod_short](includes/prod_short.md)]. Mottak og datakonvertering av PEPPOL-fakturaer utføres av rammeverket for datautveksling, representert av datautvekslingsdefinisjonen **PEPPOL - faktura**.  

  Hvis du for eksempel vil motta en faktura som et elektronisk OCR-dokument, behandler du den når du mottar et elektronisk PEPPOL-dokument. Mottak og konvertering av elektroniske dokumenter fra OCR utføres av rammeverket for datautveksling, representert av datautvekslingsdefinisjonen **OCR - faktura**.  

## Bankfiler

Filformatene for utveksling av bankdata med forretningsadministrasjonsprogrammer varierer avhengig av leverandøren av filen og landet eller regionen. [!INCLUDE[prod_short](includes/prod_short.md)] støtter import og eksport av SEPA-bankfiler (Single Euro Payments Area). I tillegg lar AMC Banking 365 Fundamentals-utvidelsen deg koble til en AMC Banking 365 Fundamentals-utvidelse som leveres av en ekstern leverandør, AMC Consult. Hvis du vil ha mer informasjon, se [Betale med AMC Banking 365 Fundamentals-utvidelsen eller SEPA-kredittoverføring](finance-make-payments-with-bank-data-conversion-service-or-sepa-credit-transfer.md). Hvis du vil ha støtte for andre elektroniske dokumentformater, kan du bruke rammeverket for datautveksling.  

Hvis du vil eksportere SEPA-kredittoverføringer, velger du **Eksporter betalinger til fil**-knappen på **Utbetalingskladd**-siden, og deretter laster du opp filen for å behandle betalinger i banken. Først må du definere forskjellige hoveddata, for eksempel bankkonto, leverandører og betalingsmåter. Datakonvertering og eksport av SEPA-bankdata utføres av en dedikert codeunit og XMLport, representert av oppsettet for bankeksport/-import for **SEPA-kredittoverføring**. Du kan eventuelt definere utvidelsen AMC Banking 365 Fundamentals til å utføre eksporten, representert av datautvekslingsdefinisjonen **AMC Banking 365 Fundamentals – kredittoverføring** .  

 Hvis du vil eksportere instruksjoner for SEPA Direct Debit, velger du **Eksporter Direct Debit-fil**-knappen på **Direct Debit-oppkrevinger**-siden, og sender deretter til banken for automatisk å samle inn de aktuelle kundebetalingene. Du må først definere bankkontoer, kunder, direct debit-belastningsfullmakter og betalingsmåter. Datakonvertering og eksport av SEPA-bankdata utføres av en dedikert codeunit og XMLport, representert av oppsettet for bankeksport/-import for **SEPA Direct Debit**.  

 Hvis du vil importere SEPA-bankkontoutdrag, kan du velge knappen Importer bankkontoutdrag på sidene **Betalingsavstemmingskladd** og **Bankkontoavstemming**, og deretter fortsette å bruke hver enkelt bankkontoutdragspost på betalinger eller bankkontoposter, manuelt eller automatisk. Du må først definere bankkontoer. Import og datakonvertering av SEPA-bankdata utføres av rammeverket for datautveksling, representert av datautvekslingsdefinisjonen **SEPA CAMT**. Du kan eventuelt definere utvidelsen AMC Banking 365 Fundamentals til å utføre importen, representert av datautvekslingsdefinisjonen **AMC Banking 365 Fundamentals – bankkontoutdrag** .  

 De lokale versjonene av [!INCLUDE[prod_short](includes/prod_short.md)] støtter i tillegg diverse andre filformater for import/eksport av bankdata, lønnstransaksjoner og andre data. Hvis du vil ha mer informasjon, kan du se målsiden [Lokal funksjonalitet](about-localization.md) for ditt land/område i hjelpen.  

## Valutakurser

Du kan definere en ekstern tjeneste for å holde valutakurser oppdatert. Tjenesten som leverer oppdaterte valutakurser, er aktivert som en datautvekslingsdefinisjon. Tilsvarende er siden **Kort for oppsett for val.kursoppdatering** en komprimert visning av siden **Datautvekslingsdefinisjon** for den aktuelle datautvekslingsdefinisjonen.  

For alle utvekslinger av data i XML-filer kan du klargjøre datautvekslingsoppsettet ved å laste inn den relaterte XML-skjemafilen på siden **Visningsprogram for XML-skjema**. Her velger du dataelementene du vil utveksle med [!INCLUDE[prod_short](includes/prod_short.md)], og deretter initialiserer du en datautvekslingsdefinisjon eller genererer en XMLport.

## Intrastat

[!INCLUDE[prod_short](includes/prod_short.md)] bruker datautvekslingsrammeverket til Intrastat-rapportering der du enkelt kan opprette tidsstemplede filer i forskjellige formater for eksport. [!INCLUDE[prod_short](includes/prod_short.md)] inneholder forberedte formater for lokaliserte land/områder og standardversjon. Du kan imidlertid endre standardrapporten eller lage din egen.

## Se også

[Utveksle data elektronisk](across-data-exchange.md)  
[Bruk XML-skjemaer til å klargjøre datautvekslingsdefinisjoner](across-how-to-use-xml-schemas-to-prepare-data-exchange-definitions.md)  
[Definere datautveksling](across-set-up-data-exchange.md)  
[Inngående dokumenter](across-income-documents.md)  
[Generelle forretningsfunksjoner](ui-across-business-areas.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
