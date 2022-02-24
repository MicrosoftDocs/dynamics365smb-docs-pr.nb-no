---
title: Rammeverket for datautveksling | Microsoft-dokumentasjon
description: Filformater for utveksling av data i bankfiler, elektroniske dokumenter, valutakurser og andre med ERP-systemer varierer avhengig av leverandøren av datafilen eller -strømmen og landet/regionen.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 01/30/2020
ms.author: sgroespe
ms.openlocfilehash: 154d72032171fa6fbe223ba4f152f868d577c8c7
ms.sourcegitcommit: d0dc5e5c46b932899e2a9c7183959d0ff37738d6
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 02/20/2020
ms.locfileid: "3076710"
---
# <a name="about-the-data-exchange-framework"></a>Rammeverket for datautveksling
Du kan bruke rammeverket for datautveksling til å utveksle forretningsdokumenter, bankfiler, valutakurser og andre datafiler med forretningspartnerne.

Som administrator eller Microsoft-partner kan du bruke rammeverket i nye integrasjonsfunksjoner ved å definere hvilke data som skal utveksles, og hvordan. Filformater for utveksling av data i bankfiler, elektroniske dokumenter, valutakurser og andre med ERP-systemer varierer for eksempel avhengig av leverandøren av datafilen eller -strømmen og landet/regionen. [!INCLUDE[d365fin](includes/d365fin_md.md)] støtter ulike bankfilformater og dataservicestandarder. Hvis du vil ha støtte for andre elektroniske dokumentformater, kan du bruke rammeverket for datautveksling.

 Diagrammene nedenfor viser arkitekturen til rammeverket for datautveksling.  

 ![Rammeverket for datautveksling &#45; Import](media/across-data-exchange/dataexchangeframework_import.png)  

 ![Rammeverket for datautveksling &#45; Eksport](media/across-data-exchange/dataexchangeframework_export.png)  

 ## <a name="electronic-documents"></a>Elektroniske dokumenter
 Som et alternativ til å sende forretningsdokumenter som filvedlegg via e-post, kan du sende og motta dem elektronisk. Med elektronisk dokument menes en standardkompatibel fil som representerer et forretningsdokument, for eksempel en faktura fra en leverandør som du kan motta og konvertere til en kjøpsfaktura i [!INCLUDE[d365fin](includes/d365fin_md.md)]. Utvekslingen av elektroniske dokumenter mellom to handelspartnere uføres ved hjelp av en ekstern leverandør av dokumentutvekslingstjenester. Den generelle versjonen av [!INCLUDE[d365fin](includes/d365fin_md.md)] kan sende og motta elektroniske fakturaer og kreditnotaer i PEPPOL-format, som støttes av de største leverandørene av dokumentutvekslingstjenester. En større leverandør av dokumentutvekslingstjenester er forhåndskonfigurert og klar til å bli definert for firmaet. Hvis du vil ha støtte for andre elektroniske dokumentformater, må du opprette nye datautvekslingsdefinisjoner ved hjelp av rammeverket for datautveksling.  

 Fra PDF- eller bildefiler som representerer inngående dokumenter, kan du få en ekstern OCR-tjeneste (optisk tegngjenkjenning) til å opprette elektroniske dokumenter som du deretter kan konvertere til dokumentposter i [!INCLUDE[d365fin](includes/d365fin_md.md)], på samme måte som for elektroniske PEPPOL-dokumenter. Når du for eksempel mottar en faktura i PDF-format fra leverandøren, kan du sende den til OCR-tjenesten fra siden **Inngående dokumenter**. Etter noen få sekunder får du filen tilbake som en elektronisk faktura som kan konverteres til en kjøpsfaktura for leverandøren. Hvis du sender filen til OCR-tjenesten via e-post, opprettes deretter en ny post for inngående dokument automatisk når du får det elektroniske dokumentet tilbake.  

 Hvis du for eksempel vil sende en salgsfaktura som et elektronisk PEPPOL-dokument, velger du alternativet **Elektronisk dokument** i dialogboksen **Bokfør og send**. Herfra kan du også angi kundens standardprofil for dokumentsending. Først må du definere forskjellige hoveddata, for eksempel firmainformasjon, kunder, varer og enheter. Disse brukes til å identifisere forretningspartnere og elementer når du konverterer data i feltene i [!INCLUDE[d365fin](includes/d365fin_md.md)] til elementene i den utgående dokumentfilen. Datakonverteringen og sendingen av PEPPOL-salgsfakturaen blir utført av dedikerte kodeenheter og XML-porter, representert av det elektronisk dokumentformatet **PEPPOL**.  

 Hvis du for eksempel vil motta en faktura fra en leverandør som et elektronisk PEPPOL-dokument, kan du behandle dokumentet på siden **Innkommende dokumenter** for å konvertere det til en kjøpsfaktura i [!INCLUDE[d365fin](includes/d365fin_md.md)]. Du kan angi jobbkøfunksjonen til å behandle slike filer med jevne mellomrom, eller du kan starte prosessen manuelt. Først må du definere forskjellige hoveddata, for eksempel firmainformasjon, leverandører, varer og enheter. Disse brukes til å identifisere forretningspartnere og elementer når du konverterer data i elementer i den innkommende dokumentfilen til felt i [!INCLUDE[d365fin](includes/d365fin_md.md)]. Mottak og datakonvertering av PEPPOL-fakturaer utføres av rammeverket for datautveksling, representert av datautvekslingsdefinisjonen **PEPPOL - faktura**.  

  Hvis du for eksempel vil motta en faktura som et elektronisk OCR-dokument, behandler du den når du mottar et elektronisk PEPPOL-dokument. Mottak og konvertering av elektroniske dokumenter fra OCR utføres av rammeverket for datautveksling, representert av datautvekslingsdefinisjonen **OCR - faktura**.  

 ## <a name="bank-files"></a>Bankfiler  
 Filformatene for utveksling av bankdata med ERP-systemer varierer avhengig av leverandøren av filen og landet eller regionen. [!INCLUDE[d365fin](includes/d365fin_md.md)] støtter import og eksport av SEPA-bankfiler (Single Euro Payments Area) og AMC Banking med utvidelsen 365 Fundamentals kan du koble til en AMC Banking med utvidelsen Fundamentals fra ekstern leverandør, AMC Consult. Hvis du vil ha støtte for andre elektroniske dokumentformater, kan du bruke rammeverket for datautveksling.  

 Hvis du vil eksportere SEPA-kredittoverføringer, velger du **Eksporter betalinger til fil**-knappen på **Utbetalingskladd**-siden, og deretter laster du opp filen for å behandle betalinger i banken. Først må du definere forskjellige hoveddata, for eksempel bankkonto, leverandører og betalingsmåter. Datakonvertering og eksport av SEPA-bankdata utføres av en dedikert codeunit og XMLport, representert av oppsettet for bankeksport/-import for **SEPA-kredittoverføring**. Du kan eventuelt definere utvidelsen AMC Banking 365 Fundamentals til å utføre eksporten, representert av datautvekslingsdefinisjonen **AMC Banking 365 Fundamentals – kredittoverføring** .  

 Hvis du vil eksportere instruksjoner for SEPA Direct Debit, velger du **Eksporter Direct Debit-fil**-knappen på **Direct Debit-oppkrevinger**-siden, og sender deretter til banken for automatisk å samle inn de aktuelle kundebetalingene. Du må først definere bankkontoer, kunder, direct debit-belastningsfullmakter og betalingsmåter. Datakonvertering og eksport av SEPA-bankdata utføres av en dedikert codeunit og XMLport, representert av oppsettet for bankeksport/-import for **SEPA Direct Debit**.  

 Hvis du vil importere SEPA-bankkontoutdrag, kan du velge knappen Importer bankkontoutdrag på sidene **Betalingsavstemmingskladd** og **Bankkontoavstemming**, og deretter fortsette å bruke hver enkelt bankkontoutdragspost på betalinger eller bankkontoposter, manuelt eller automatisk. Du må først definere bankkontoer. Import og datakonvertering av SEPA-bankdata utføres av rammeverket for datautveksling, representert av datautvekslingsdefinisjonen **SEPA CAMT**. Du kan eventuelt definere utvidelsen AMC Banking 365 Fundamentals til å utføre importen, representert av datautvekslingsdefinisjonen **AMC Banking 365 Fundamentals – bankkontoutdrag** .  

 De lokale versjonene av [!INCLUDE[d365fin](includes/d365fin_md.md)] støtter i tillegg diverse andre filformater for import/eksport av bankdata, lønnstransaksjoner og andre data. Hvis du vil ha mer informasjon, se hjelpen for "Lokal funksjonalitet" i ditt lands versjon av [!INCLUDE[d365fin](includes/d365fin_md.md)].

  ## <a name="currency-exchange-rates"></a>Valutakurser  
 Du kan definere en ekstern tjeneste for å holde valutakurser oppdatert. Tjenesten som leverer oppdaterte valutakurser, er aktivert som en datautvekslingsdefinisjon. Tilsvarende er siden **Kort for oppsett for val.kursoppdatering** en komprimert visning av siden **Datautvekslingsdefinisjon** for den aktuelle datautvekslingsdefinisjonen.  

 For alle utvekslinger av data i XML-filer kan du klargjøre datautvekslingsoppsettet ved å laste inn den relaterte XML-skjemafilen på siden **Visningsprogram for XML-skjema**. Her velger du dataelementene du vil utveksle med [!INCLUDE[d365fin](includes/d365fin_md.md)], og deretter initialiserer du en datautvekslingsdefinisjon eller genererer en XMLport.

## <a name="see-also"></a>Se også  
[Utveksle data elektronisk](across-data-exchange.md)  
[Bruke XML-skjemaer til å klargjøre datautvekslingsdefinisjoner](across-how-to-use-xml-schemas-to-prepare-data-exchange-definitions.md)  
[Definere datautveksling](across-set-up-data-exchange.md)  
[Inngående dokumenter](across-income-documents.md)  
[Generelle forretningsfunksjoner](ui-across-business-areas.md)  
