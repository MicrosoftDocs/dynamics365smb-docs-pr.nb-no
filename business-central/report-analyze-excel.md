---
title: Analyser rapportdata med Excel og XML
description: Finn ut hvordan du bruker Excel og XML til å analysere et rapportdatasett.
author: jswymer
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 'task, process, report, print, schedule, save, Excel, PDF, Word, dataset'
ms.date: 03/16/2022
ms.author: jswymer
---
# <a name="analyzing-report-data-with-excel-and-xml"></a><a name="analyzing-report-data-with-excel-and-xml"></a>Analyser rapportdata med Excel og XML

[!INCLUDE[2021_releasewave2](includes/2021_releasewave2.md)]

Som utvikler eller avansert bruker bidrar det til å kontrollere dataene som genereres for et gitt rapportdatasett mens du oppretter nye rapporter eller endrer eksisterende rapporter. For å støtte denne funksjonen kan du eksportere et rapportdatasett som rådata til et Excel-regneark eller XML-fil – direkte. I Excel kan du for eksempel foreta ad hoc-analysere av dataene og diagnostisere problemer.

## <a name="get-started"></a><a name="get-started"></a>Kom i gang

Hvis du vil eksportere et rapportdatasett til et Excel-arbeidsbok eller XLM-fil, åpner du rapporten i klienten og velger **Send til** > **Microsoft Excel-dokument (bare data)** eller **XML-dokument**. Filen lastes ned til enheten.

## <a name="more-about-excel-data-only"></a><a name="more-about-excel-data-only"></a>Mer om Excel (bare data)

Alternativet **Microsoft Excel-dokument (bare data)** eksporterer rapportresultatene og kriteriene som ble brukt til å generere dem, men de inneholder ikke rapportoppsettet. Excel-filen vil inneholde hele datasettet, som rådata, ordnet i rader og kolonner. Alle datakolonnene i datasettet til rapporten inkluderes, uavhengig av om de brukes i rapportoppsettet.

Når du har Excel-filen, kan du begynne å analysere dataene. Du kan for eksempel filtrere dataene og bruke Power Pivot til å vise dem.

Hver gang du eksporterer resultater, opprettes et nytt regneark. Ved hjelp av alternativet **Microsoft Excel-dokument (bare data)** kan du kjøre samme rapport og bruke formateringsendringer på nytt. Du kan for eksempel for Power Pivot kjøre rapporten på nytt i en annen tidsperiode, kopiere resultatene til regnearket og deretter oppdatere regnearket. Du kan også finne en rapporteringsapp i [AppSource](https://appsource.microsoft.com/).

> [!NOTE]
> Du kan ikke eksportere en rapport som har mer enn 1 048 576 rader eller 16 384 kolonner. Med Business Central lokal kan maksimalt antall eksporterte rader være enda mindre. Business Central Server inneholder en konfigurasjonsinnstilling **Maks datarader som tillates å sende til Excel**, for å redusere grensen fra maksimumsverdien. Hvis du vil ha mer informasjon, kan du se [Konfigurere Business Central Server](/dynamics365/business-central/dev-itpro/administration/configure-server-instance#General) eller kontakte systemansvarlig.

## <a name="for-administrators"></a><a name="for-administrators"></a>For systemansvarlige

- **Microsoft Excel-dokument (bare data)** ble introdusert som en valgfri funksjon i 2021 lanseringsbølge 1, oppdatering 18.3. Hvis du vil gi brukere tilgang til denne funksjonen når du kjører lanseringsbølge 1 for 2021, aktiverer du funksjonsoppdateringen **Lagre rapportdatasett i Microsoft Excel-dokument** i **Funksjonsstyring**. Hvis du vil ha mer informasjon, kan du se [Aktivering av kommende funksjoner på forhånd](/dynamics365/business-central/dev-itpro/administration/feature-management). I 2021 lanseringsbølge 2 ble denne funksjonen permanent, slik at du ikke trenger å aktivere den.

- Hvis du vil bruke **Microsoft Excel-dokument (bare data)**, trenger brukerkontoer tillatelsen **Tillat handlingen Eksporter rapportdatasett i Excel**. Du kan gi brukerne denne tillatelsen ved å tilordne **feilsøkingsverktøyene** eller tillatelsessettet **Eksporter rapport Excel**. Hvis du vil ha mer informasjon, kan du se [Tilordne tillatelser til brukere og grupper](ui-define-granular-permissions.md).  

## <a name="for-developers-and-advanced-users"></a><a name="for-developers-and-advanced-users"></a>For utviklere og avanserte brukere

Alternativet **Microsoft Excel-dokument (bare data)** eksporterer alle kolonner, inkludert kolonner som inneholder filtre og formateringsinstruksjoner for andre verdier. Her er noen viktige punkter:

- Binære data i et felt, for eksempel et bilde, eksporteres ikke.

  I kolonner som inneholder binære data, inneholder feltet **Binære data ({0} byte)**, der **{0}** indikerer antall byte.
- Fra og med Business Central 2021 lanseringsbølge 2 inneholder Excel-filen også regnearket **Rapportmetadata**.

  Dette regnearket viser hvilke filtre som er brukt på rapporten og egenskaper for den generelle rapporten, for eksempel navn, ID og utvidelsesinformasjon. Filtrene vises i **Filter (DataItem::Table::FilterGroupNo::FieldName)**-kolonnen. Filtrene i denne kolonnen inkluderer filtre som er angitt på forespørselssiden for rapporten. Det inneholder også filtre som er definert i AL-kode, for eksempel av [egenskapen DataItemLink](/dynamics365/business-central/dev-itpro/developer/properties/devenv-dataitemlink-reports-property) og [egenskapen DataItemTableView](/dynamics365/business-central/dev-itpro/developer/properties/devenv-dataitemtableview-property).

Hvis du vil ha mer informasjon om rapportutforming, kan du se [Rapportoversikt](/dynamics365/business-central/dev-itpro/developer/devenv-reports).

## <a name="see-also"></a><a name="see-also"></a>Se også

[Arbeid med rapporter](ui-work-report.md)  
[Administrere rapport- og dokumentoppsett](ui-manage-report-layouts.md)  
[Tilordne tillatelser til brukere og grupper](ui-define-granular-permissions.md)  
[Arbeide med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)

[!INCLUDE[footer-include](includes/footer-banner.md)]
