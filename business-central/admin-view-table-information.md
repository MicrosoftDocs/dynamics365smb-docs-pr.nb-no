---
title: Vis Tabellinformasjon
description: Lær hvordan du kan vise informasjon om databasetabellene i Business Central.
author: jswymer
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.form: 8700
ms.date: 08/23/2022
ms.author: jswymer
---

# <a name="viewing-table-information" />Vise Tabellinformasjon

Siden **8700 Tabellinformasjon** inneholder informasjon om antall poster i alle system- og forretningstabeller i [!INCLUDE[prod_short](includes/prod_short.md)] og hvor mye data hver tabell inneholder.

Denne informasjonen er nyttig for å feilsøke ytelsesproblemer, siden dette gir deg muligheten til å se fordelingen av datastørrelsen på tvers av tabeller.

## <a name="viewing-table-information" />Vise tabellinformasjon

Du kan åpne denne siden ved å velge ikonet ![Søk etter side eller rapport.](media/ui-search/search_small.png "Ikonet Søk etter side eller rapport") og angi **Tabellinformasjon**, og velg deretter den relaterte koblingen.

Følgende tabell beskriver opplysningene som er gitt for hver tabell:

|Kolonne|Beskrivelse|
|------|-----------|
|Selskapsnavn|Navnet på selskapet (hvis noen) som tabellen tilhører.|
|Tabellnavn|Navnet på tabellen.|
|Tabellnr.|ID-en for tabellen.|
|Nr. poster|Totalt antall poster lagret i tabellen.|
|Poststørrelse|Gjennomsnittlig poststørrelse i kB/post. Verdien beregnes ved hjelp av følgende formel: 1024 (størrelse)/(antall poster). |
|Størrelse (kB)|Hvor mye plass tabellen opptar i databasen totalt. Denne verdien er summen av verdiene i feltene Datastørrelse og Indeksstørrelse.|
|Datastørrelse (kB)|Hvor mye plass dataene i tabellen opptar i databasen.|
|Indeksstørrelse (kB)|Hvor mye plass tabellindeksene (nøkler) opptar i databasen.|
|Komprimering|Komprimeringstypen, **Rad**, **Side** eller **Ingen** som brukes på tabellen i databasen. Hvis du vil ha mer informasjon, kan du se [Datakomprimering](/sql/relational-databases/data-compression/data-compression?).|

> [!NOTE]
> Hvis du sletter data i en tabell, starter [!INCLUDE[prod_short](includes/prod_short.md)] flere prosesser i bakgrunnen for å sikre at alt fjernes i databasen. Verdiene på siden Tabellinformasjon oppdateres ikke før disse prosessene er fullført, noe som kan ta litt tid. Hvor lang tid du må vente, kan variere avhengig av størrelsen på databasen.

## <a name="see-also" />Se også

[Kontrollere sider](across-inspect-page.md)  
[Ytelsesartikler for utviklere](/dynamics365/business-central/dev-itpro/performance/performance-developer)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
