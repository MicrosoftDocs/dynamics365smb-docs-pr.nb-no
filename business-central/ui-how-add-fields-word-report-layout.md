---
title: Legge til felt i et Word-rapportoppsett
description: Dette emnet beskriver hvordan du legger til felt i et rapportdatasett i et eksisterende Word-rapportoppsett for en rapport.
author: jswymer
ms.topic: conceptual
ms.devlang: al
ms.search.keywords: null
ms.date: 11/25/2021
ms.author: jswymer
ms.service: dynamics-365-business-central
---

# Arbeid med Word-oppsett

Et oppsett i et Word-rapport angir innholdet i og formatet for en rapport når den forhåndsvises og skrives ut fra Business Central. Du oppretter og endrer disse oppsettene i Microsoft Word.

[![Eksempel på et Word-rapportoppsettsdokument for Business Central.](media/word-layout.png)](media/word-layout.png#lightbox) 

Når du endrer et Word-rapportoppsett, kan du angi feltene i datasettet i rapporten som skal tas med i rapporten, og hvordan feltene er ordnet. Du definerer også det generelle formatet for rapporten, for eksempel skrifttype, størrelse, marger og bakgrunnsbilder. Du skal vanligvis ordne innholdet i rapporten ved å legge til tabeller i oppsettet.

For å foreta generelle formaterings- og oppsettsendringer, for eksempel endre skrift, legge til eller endre en tabell eller fjerne et datafelt, bruker du bare de grunnleggende redigeringsfunksjonene i Word, som du gjør med et Word-dokument.

Hvis du utformer et Word-rapportoppsett fra grunnen av eller legger til nye datafelt, begynner du med å legge til en tabell som inneholder rader og kolonner som omsider skal inneholde datafeltene.

> [!TIP]  
> Vis tabellrutenettet, slik at du kan se cellegrensene i tabellen. Husk å skjule rutenettet når du er ferdig å redigere. Hvis du vil vise eller skjule tabellrutenett, merker du tabellen. Under **Oppsett** i kategorien **Tabell** velger du deretter **Vis rutenettlinjer**.

## Bygge inn skrifter i Word-oppsett for konsekvens

Hvis du vil sikre at rapporter alltid vises og skrives ut med de tiltenkte skriftene, uansett hvor brukere åpner eller skriver ut rapporter, kan du bygge inn skrifter i Word-dokumentet. Innebygde skrifter kan imidlertid øke størrelsen på Word-filer betydelig. Hvis du vil ha mer informasjon om innebygging av skrifter i Word, se [Bygge inn skrifter i Word, PowerPoint eller Excel](https://support.office.com/article/Embed-fonts-in-Word-PowerPoint-or-Excel-cb3982aa-ea76-4323-b008-86670f222dbc).

## Legge til datafelt

Et rapportdatasett kan bestå av felt som viser etiketter, data og bilder. Dette emnet beskriver fremgangsmåten for å legge til felt i et rapportdatasett i et eksisterende Word-rapportoppsett for en rapport. Du legger til felt ved hjelp av den egendefinerte XML-delen for Word for rapporten og ved å legge til innholdskontroller som tilordnes til feltene i rapportdatasettet. Når du skal legge til feltene, må du ha noe kjennskap til rapportens datasett, slik at du kan identifisere hvilke felt du vil legge til i oppsettet.  
  
> [!NOTE]  
>  Du kan ikke endre innebygde rapportoppsett<!--Onprem. Built-in layouts can only be modified by using the development environment-->.  

###  <a name="OpenXMLPart"></a> Åpne den egendefinerte XML-delen for rapporten i Word  
  
1. Åpne Word-rapportoppsettdokumentet i Word hvis det ikke allerede er åpent.  
  
     Hvis du vil ha mer informasjon, kan du se [Opprette og endre et egendefinert rapportoppsett](ui-how-create-custom-report-layout.md).  
  
2. Vis fanebladet **Utvikler** på båndet i Microsoft Word.  
  
     Fanebladet **Utvikler** vises som standard ikke på båndet. Hvis du vil ha mer informasjon, kan du se [Vise fanebladet Utvikler på båndet](/visualstudio/vsto/how-to-show-the-developer-tab-on-the-ribbon).  
  
3. Velg **XML-tilordningsrute** i fanebladet **Utvikler**.  
  
4. I ruten **XML-tilordning**, i **Tilpass XML-del**-nedtrekkslisten, velger du den egendefinerte XML-delen for [!INCLUDE[prod_short](includes/prod_short.md)]-rapporten, som vanligvis er den siste i listen. Navnet på den egendefinerte XML-delen har følgende format:  
  
     `urn:microsoft-dynamics-nav/reports/<report_name>/<ID>`  

     `<report_name>` er navnet som er tilordnet til rapporten 

     `<ID>` er identifikasjonsnummeret til rapporten.  
  
     Når du har valgt den egendefinerte XML-delen, vises etikettene og feltkontrollene som er tilgjengelige for rapporten, i ruten XML-tilordning.  
  
### Legge til en etikett eller et datafelt  
  
1. Plasser markøren i dokumentet der du vil legge til kontrollen.  
  
2. Høyreklikk kontrollen du vil legge til, i ruten **XML-tilordning**. Velg **Sett inn innholdskontroll**, og velg deretter **Ren tekst**.  
  
    > [!NOTE]  
    >  Du kan ikke legge til et felt ved å skrive inn navnet på datasettet manuelt i innholdskontrollen. Du må bruke **XML-tilordning**-ruten for å tilordne feltene.  
  
### Legge til gjentatte rader med datafelt til å opprette en liste  
  
1. Legg til en tabellrad som inneholder en kolonne for hvert felt du vil gjenta, i en tabell.  
  
   Denne raden vil fungere som en plassholder for gjentatte felt.  
  
2. Merk hele raden.  
  
3. Høyreklikk kontrollen som svarer til rapportdataelementet som inneholder feltene du vil gjenta, i ruten **XML-tilordning**. Velg **Sett inn innholdskontroll**, og velg deretter **Gjentatt**.  
  
4. Legg til gjentatte felt i raden slik:  
  
    1. Plasser pekeren i en kolonne.  
  
    2. Høyreklikk kontrollen du vil legge til, i ruten **XML-tilordning**. Velg **Sett inn innholdskontroll**, og velg deretter **Ren tekst**.  
  
    3. Gjenta trinn a og b for hvert felt.  
  
## Legg til bildefelter

En datasettrapport kan ha et felt som inneholder et bilde, for eksempel en firmalogo eller et bilde av en vare. Hvis du vil legge til et bilde fra rapportdatasettet, setter du inn en **Bilde**-innholdskontroll.  
  
Bilder justeres etter øvre venstre hjørne i innholdskontrollen og får størrelsen endret automatisk slik at de passer i rammen rundt innholdskontrollen.  
  
> [!IMPORTANT]  
> Du kan bare legge til bilder som har et format som støttes av Word, for eksempel filtypene BMP, JPEG og PNG. Hvis du legger til et bilde med et format som ikke støttes av Word, får du en feilmelding når du kjører rapporten fra [!INCLUDE[prod_short](includes/prod_short.md)]-klienten.  
  
### Legge til et bilde  
  
1. Plasser pekeren i dokumentet der du vil legge til kontrollen.  
  
2. Høyreklikk kontrollen du vil legge til, i ruten **XML-tilordning**. Velg **Sett inn innholdskontroll**, og velg deretter **Bilde**.  
  
3. Hvis du vil øke eller redusere bildestørrelsen, kan du dra et skaleringshåndtak bort fra eller mot midten av innholdskontrollen.  

##  <a name="RemoveField"></a> Fjern etikett- og datafelter

Etikett- og datafelt i en rapport er i innholdskontroller i Word. Den følgende illustrasjonen viser en innholdskontroll når den er valgt i Word-dokumentet.  

![Innholdskontroll for felt i Word-rapportoppsett.](media/nav_wordreportlayouts_contentcontrol.png "NAV_WordReportLayouts_ContentControl")  

Navnet på etiketten eller datafeltnavnet vises i innholdskontrollen. I dette eksemplet er feltnavnet CompanyAddr1.  

### Fjerne en etikett eller et datafelt  

1. Høyreklikk feltet som du vil slette, og velg deretter **Fjern innholdskontroll**.  

     Innholdskontrollen fjernes, men feltnavnet blir stående som tekst.  

2. Slett den gjenstående teksten etter behov.

## Oversikt over tilpassing av XML-del

Word-rapportoppsett er bygd på *egendefinerte XML-deler*. En egendefinert XML-del for en rapport består av elementer som svarer til dataelementer, kolonner og etiketter som utgjør rapportens datasett. <!--OnPrem The data as defined in the Report Dataset Designer in Microsoft Dynamics NAV Development Environment. -->Den egendefinerte XML-delen brukes til å tilordne dataene til en rapport når rapporten kjøres.

### XML-struktur for egendefinert XML-del

Tabellen nedenfor gir en forenklet oversikt over XML-filen for en egendefinert XML-del.  
  
|XML-elementer|Beskrivelse|  
|------------------|-----------------|  
|`<?xml version="1.0" encoding="utf-16"?>`|Overskrift|  
|`<WordReportXmlPart xmlns="urn:microsoft-dynamics-365/report/<reportname>/<id>/"`|Spesifikasjon av XML-navneområde. `<reportname>` er navnet som er tilordnet til rapporten. `<id>` er ID-en som er tilordnet til rapporten.|  
|`..<Labels>`<br /><br /> `....<ColumnNameCaption>ColumnNameCaption</ColumnNameCaption>`<br /><br /> `....<LabelName>LabelCaption</LabelName>`<br /><br /> `..</Labels>`|Inneholder alle etikettene for rapporten.<!--OnPren The element includes labels that are related to columns that have the IncludeCaption Property.--><br />-   Etikettelementer som er knyttet til kolonner, har formatet `<ColumnNameCaption>ColumnNameCaption</ColumnNameCaption>`.<!--OnPrem where `ColumnName` is determined by the column's Name Property.-->.<br />- Etikettelementer har formatet `<LabelName>LabelName</LabelName`<!--OnPrem where LabelName is determined by the label's Name Property.-->.<br />-   Etiketter er oppført i alfabetisk rekkefølge.|  
|`..<DataItem1>`<br /><br /> `....<DataItem1Column1>DataItem1Column1</DataItem1Column1>`|Dataelement og kolonner på øverste nivå. Kolonner er oppført i alfabetisk rekkefølge.<!--OnPrem <br /><br /> The element names and values are determined by the Name Property of the data item or column.-->|  
|`....<DataItem2>`<br /><br /> `......<DataItem2Column1>DataItem2Column1</DataItem2Column1>`<br /><br /> `....</DataItem2>`<br /><br /> `....<DataItem3>`<br /><br /> `......<DataItem3Column1>DataItem3Column1</DataItem3Column1>`<br /><br /> `....</DataItem3>`|Dataelementer og kolonner som er nestet i dataelementet på øverste nivå. Kolonner er oppført i alfabetisk rekkefølge under det respektive dataelementet.|  
|`..</DataItem1>`<br /><br /> `</WordReportXmlPart>`|Avsluttende element.|  
  
### Egendefinert XML-del i Word

 Åpne den egendefinerte XML-delen i ruten **XML-tilordning** i Word, og bruk deretter ruten til å tilordne elementer til innholdskontroller i Word-dokumentet. Ruten **XML-tilordning** er tilgjengelig i fanebladet **Utvikler**. (Hvis du vil ha mer informasjon, kan du se [Vise fanebladet Utvikler på båndet](/visualstudio/vsto/how-to-show-the-developer-tab-on-the-ribbon)).  
  
 Elementene i **XML-tilordning**-ruten vises i en struktur som ligner på XML-kilden. Etikettfelt er gruppert under et felles **Etiketter**-element, og dataelementer og kolonner er ordnet i en hierarkisk struktur som svarer til XML-kilden, med kolonner i alfabetisk rekkefølge. Elementer identifiseres ved kolonnenavn i henhold til rapportens datasett i AL-kode. Hvis du vil ha mer informasjon, kan du se [Definering av et rapportdatasett](/dynamics365/business-central/dev-itpro/developer/devenv-report-dataset).  
  
 Den følgende illustrasjonen viser den egendefinerte XML-delen fra forrige inndeling i **XML-tilordning**-ruten i et Word-dokument.  
  
 ![Klipp av ruten XML-tilordning i Word.](media/nav_reportlayout_xmlmappingpane.png "NAV_ReportLayout_XMLMappingPane")  
  
* Hvis du vil legge til en etikett eller et felt i oppsettet, setter du inn en innholdskontroll som tilordnes til elementet i **XML-tilordning**-ruten.  
  
* Hvis du vil opprette gjentagende rader med kolonner, kan du sette inn en **gjentagende** innholdskontroll for det overordnede dataelementet og deretter legge til innholdskontrollen for kolonnene.  
  
* Når det gjelder etiketter, er den faktiske teksten som vises i den genererte rapporten, verdien til egenskapen **Caption** for feltet i dataelementtabellen (hvis etiketten er knyttet til kolonnen i rapportdatasettet), eller en etikett i Report Label Designer (hvis etiketten ikke er knyttet til en kolonne i datasettet).  
  
* Språket på etiketten som vises når du kjører rapporten, avhenger av språkinnstillingen for rapportobjektet.  
  
## Se også

[Opprette og endre et egendefinert rapportoppsett](ui-how-create-custom-report-layout.md)   


[!INCLUDE[footer-include](includes/footer-banner.md)]