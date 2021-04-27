---
title: Legge til felt i et Word-rapportoppsett | Microsoft-dokumentasjon
description: Beskriver hvordan du legger til felt i et rapportdatasett i et eksisterende Word-rapportoppsett for en rapport.
author: jswymer
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/01/2021
ms.author: jswymer
ms.openlocfilehash: 52cfb4ba4ca0ba645ecca48e08d63722c2c5c5b4
ms.sourcegitcommit: 766e2840fd16efb901d211d7fa64d96766ac99d9
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 03/31/2021
ms.locfileid: "5771113"
---
# <a name="add-fields-to-a-word-report-layout"></a>Legge til felt i et Word-rapportoppsett
Et rapportdatasett kan bestå av felt som viser etiketter, data og bilder. Dette emnet beskriver fremgangsmåten for å legge til felt i et rapportdatasett i et eksisterende Word-rapportoppsett for en rapport. Du legger til felt ved hjelp av den egendefinerte XML-delen for Word for rapporten og ved å legge til innholdskontroller som tilordnes til feltene i rapportdatasettet. Når du skal legge til feltene, må du ha noe kjennskap til rapportens datasett, slik at du kan identifisere hvilke felt du vil legge til i oppsettet.  
  
> [!NOTE]  
>  Du kan ikke endre innebygde rapportoppsett<!--Onprem. Built-in layouts can only be modified by using the development environment-->.  

##  <a name="to-open-the-custom-xml-part-for-the-report-in-word"></a><a name="OpenXMLPart"></a> Åpne den egendefinerte XML-delen for rapporten i Word  
  
1.  Åpne Word-rapportoppsettdokumentet i Word hvis det ikke allerede er åpent.  
  
     Hvis du vil ha mer informasjon, kan du se [Opprette og endre et egendefinert rapportoppsett](ui-how-create-custom-report-layout.md).  
  
2.  Vis fanebladet **Utvikler** på båndet i Microsoft Word.  
  
     Fanebladet **Utvikler** vises som standard ikke på båndet. Hvis du vil ha mer informasjon, kan du se [Vise fanebladet Utvikler på båndet](/visualstudio/vsto/how-to-show-the-developer-tab-on-the-ribbon).  
  
3.  Velg **XML-tilordningsrute** i fanebladet **Utvikler**.  
  
4.  I ruten **XML-tilordning** i rullegardinlisten **Egendefinert XML-del** velger den egendefinerte XML-delen for ADD INCLUDE-rapporten,<!--[!INCLUDE[prod_short](../../includes/prod_short.md)]--> som vanligvis er sist i oversikten. Navnet på den egendefinerte XML-delen har følgende format:  
  
     urn:microsoft-dynamics-nav/reports/*rapportnavn*/*ID*  
  
     *rapportnavn* er navnet som er tilordnet til rapporten<!--OnPrem as specified by the report's [Name Property-duplicate](../FullExperience/nav_dev_long_md.md)]-->.  
  
     *ID* er identifikasjonsnummeret til rapporten.  
  
     Når du har valgt den egendefinerte XML-delen, vises etikettene og feltkontrollene som er tilgjengelige for rapporten, i ruten XML-tilordning.  
  
### <a name="to-add-a-label-or-data-field"></a>Legge til en etikett eller et datafelt  
  
1.  Plasser markøren i dokumentet der du vil legge til kontrollen.  
  
2.  Høyreklikk kontrollen du vil legge til, i ruten **XML-tilordning**. Velg **Sett inn innholdskontroll**, og velg deretter **Ren tekst**.  
  
    > [!NOTE]  
    >  Du kan ikke legge til et felt ved å skrive inn navnet på datasettet manuelt i innholdskontrollen. Du må bruke **XML-tilordning**-ruten for å tilordne feltene.  
  
### <a name="to-add-repeating-rows-of-data-fields-to-create-a-list"></a>Legge til gjentatte rader med datafelt til å opprette en liste  
  
1.  Legg til en tabellrad som inneholder en kolonne for hvert felt du vil gjenta, i en tabell.  
  
     Denne raden vil fungere som en plassholder for gjentatte felt.  
  
2.  Merk hele raden.  
  
3.  Høyreklikk kontrollen som svarer til rapportdataelementet som inneholder feltene du vil gjenta, i ruten **XML-tilordning**. Velg **Sett inn innholdskontroll**, og velg deretter **Gjentatt**.  
  
4.  Legg til gjentatte felt i raden slik:  
  
    1.  Plasser pekeren i en kolonne.  
  
    2.  Høyreklikk kontrollen du vil legge til, i ruten **XML-tilordning**. Velg **Sett inn innholdskontroll**, og velg deretter **Ren tekst**.  
  
    3.  Gjenta trinn a og b for hvert felt.  
  
## <a name="adding-image-fields"></a>Legge til bildefelter  
 En datasettrapport kan ha et felt som inneholder et bilde, for eksempel en firmalogo eller et bilde av en vare. Hvis du vil legge til et bilde fra rapportdatasettet, setter du inn en **Bilde**-innholdskontroll.  
  
 Bilder justeres etter øvre venstre hjørne i innholdskontrollen og får størrelsen endret automatisk slik at de passer i rammen rundt innholdskontrollen.  
  
> [!IMPORTANT]  
>  Du kan bare legge til bilder som har et format som støttes av Word, for eksempel filtypene BMP, JPEG og PNG. Hvis du legger til et bilde med et format som ikke støttes av Word, får du en feilmelding når du kjører rapporten fra ADD INCLUDE<!--[!INCLUDE[prod_short](../../includes/prod_short.md)]--> -klienten.  
  
#### <a name="to-add-an-image"></a>Legge til et bilde  
  
1.  Plasser pekeren i dokumentet der du vil legge til kontrollen.  
  
2.  Høyreklikk kontrollen du vil legge til, i ruten **XML-tilordning**. Velg **Sett inn innholdskontroll**, og velg deretter **Bilde**.  
  
3.  Hvis du vil øke eller redusere bildestørrelsen, kan du dra et skaleringshåndtak bort fra eller mot midten av innholdskontrollen.  

## <a name="custom-xml-part-overview"></a>Oversikt over tilpassing av XML-del
Word-rapportoppsett er bygd på *egendefinerte XML-deler*. En egendefinert XML-del for en rapport består av elementer som svarer til dataelementer, kolonner og etiketter som utgjør rapportens datasett. <!--OnPrem The data as defined in the Report Dataset Designer in Microsoft Dynamics NAV Development Environment. -->Den egendefinerte XML-delen brukes til å tilordne dataene til en rapport når rapporten kjøres.

  
### <a name="xml-structure-of-custom-xml-part"></a>XML-struktur for egendefinert XML-del  
Tabellen nedenfor gir en forenklet oversikt over XML-filen for en egendefinert XML-del.  
  
|XML-elementer|Beskrivelse|  
|------------------|-----------------|  
|`<?xml version="1.0" encoding="utf-16"?>`|Overskrift|  
|`<WordReportXmlPart xmlns="urn:microsoft-dynamics-365/report/<reportname>/<id>/"`|Spesifikasjon av XML-navneområde. `<reportname>` er navnet som er tilordnet til rapporten. `<id>` er ID-en som er tilordnet til rapporten.|  
|`..<Labels>`<br /><br /> `....<ColumnNameCaption>ColumnNameCaption</ColumnNameCaption>`<br /><br /> `....<LabelName>LabelCaption</LabelName>`<br /><br /> `..</Labels>`|Inneholder alle etikettene for rapporten.<!--OnPren The element includes labels that are related to columns that have the IncludeCaption Property.--><br />-   Etikettelementer som er knyttet til kolonner, har formatet `<ColumnNameCaption>ColumnNameCaption</ColumnNameCaption>`.<!--OnPrem where `ColumnName` is determined by the column's Name Property.-->.<br />- Etikettelementer har formatet `<LabelName>LabelName</LabelName`<!--OnPrem where LabelName is determined by the label's Name Property.-->.<br />-   Etiketter er oppført i alfabetisk rekkefølge.|  
|`..<DataItem1>`<br /><br /> `....<DataItem1Column1>DataItem1Column1</DataItem1Column1>`|Dataelement og kolonner på øverste nivå. Kolonner er oppført i alfabetisk rekkefølge.<!--OnPrem <br /><br /> The element names and values are determined by the Name Property of the data item or column.-->|  
|`....<DataItem2>`<br /><br /> `......<DataItem2Column1>DataItem2Column1</DataItem2Column1>`<br /><br /> `....</DataItem2>`<br /><br /> `....<DataItem3>`<br /><br /> `......<DataItem3Column1>DataItem3Column1</DataItem3Column1>`<br /><br /> `....</DataItem3>`|Dataelementer og kolonner som er nestet i dataelementet på øverste nivå. Kolonner er oppført i alfabetisk rekkefølge under det respektive dataelementet.|  
|`..</DataItem1>`<br /><br /> `</WordReportXmlPart>`|Avsluttende element.|  
  
### <a name="custom-xml-part-in-word"></a>Egendefinert XML-del i Word  
 Åpne den egendefinerte XML-delen i ruten **XML-tilordning** i Word, og bruk deretter ruten til å tilordne elementer til innholdskontroller i Word-dokumentet. Ruten **XML-tilordning** er tilgjengelig i fanebladet **Utvikler**. (Hvis du vil ha mer informasjon, kan du se [Vise fanebladet Utvikler på båndet](/visualstudio/vsto/how-to-show-the-developer-tab-on-the-ribbon)).  
  
 Elementene i **XML-tilordning**-ruten vises i en struktur som ligner på XML-kilden. Etikettfelt er gruppert under et felles **Etiketter**-element, og dataelementer og kolonner er ordnet i en hierarkisk struktur som svarer til XML-kilden, med kolonner i alfabetisk rekkefølge. Elementer identifiseres ved navn i henhold til egenskapen Name i Report Dataset Designer i ADD INCLUDE<!--[!INCLUDE[nav_dev_short](../../includes/nav_dev_short_md.md)]-->.  
  
 Den følgende illustrasjonen viser den egendefinerte XML-delen fra forrige inndeling i **XML-tilordning**-ruten i et Word-dokument.  
  
 ![Klipp av ruten XML-tilordning i Word](media/nav_reportlayout_xmlmappingpane.png "NAV_ReportLayout_XMLMappingPane")  
  
-   Hvis du vil legge til en etikett eller et felt i oppsettet, setter du inn en innholdskontroll som tilordnes til elementet i **XML-tilordning**-ruten.  
  
-   Hvis du vil opprette gjentagende rader med kolonner, kan du sette inn en **gjentagende** innholdskontroll for det overordnede dataelementet og deretter legge til innholdskontrollen for kolonnene.  
  
-   Når det gjelder etiketter, er den faktiske teksten som vises i den genererte rapporten, verdien til egenskapen **Caption** for feltet i dataelementtabellen (hvis etiketten er knyttet til kolonnen i rapportdatasettet), eller en etikett i Report Label Designer (hvis etiketten ikke er knyttet til en kolonne i datasettet).  
  
-   Språket på etiketten som vises når du kjører rapporten, avhenger av språkinnstillingen for rapportobjektet.  
  
## <a name="see-also"></a>Se også  
 [Opprette og endre et egendefinert rapportoppsett](ui-how-create-custom-report-layout.md)   


[!INCLUDE[footer-include](includes/footer-banner.md)]