---
title: Vis Tabellinformasjon
author: jswymer
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.date: 04/20/2020
ms.author: jswymer
ms.openlocfilehash: de93063a60e6b64405b1491a67489c8bfa4657ad
ms.sourcegitcommit: 99915b493a7e49d12c530f2f9fda1fcedb518b6e
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 04/21/2020
ms.locfileid: "3275321"
---
# <a name="viewing-table-information"></a>Vise Tabellinformasjon

Siden **Informasjon om 8700-tabellen** inneholder informasjon om alle system- og forretningstabeller i en Business Central-løsning. Siden viser spesielt informasjon om mengden data som tabellene inneholder.

Denne informasjonen er nyttig for å feilsøke ytelsesproblemer, siden dette gir deg muligheten til å se fordelingen av datastørrelsen på tvers av tabeller.

## <a name="viewing-table-information"></a>Vise tabellinformasjon

For å åpne denne siden velger du ![Søk etter side eller rapport](media/ui-search/search_small.png "Ikonet Søk etter side eller rapport"), angir **Tabellinformasjon** og velger deretter den relaterte koblingen.

Følgende tabell beskriver opplysningene som er gitt for hver tabell:

|Kolonne|Beskrivelse|
|------|-----------|
|Selskapsnavn|Navnet på selskapet (hvis noen) som tabellen tilhører.|
|Tabellnavn|Navnet på tabellen.|
|Tabellnr.|ID-en for tabellen|
|Antall poster|Totalt antall poster lagret i tabellen.|
|Poststørrelse|Gjennomsnittlig poststørrelse i kB/post. Verdien beregnes ved å bruke følgende formel: 1024(størrelse)/(antall poster). |

## <a name="see-also"></a>Se også

[Kontrollere sider](across-inspect-page.md)  
[Ytelsesartikler for utviklere](/dynamics365/business-central/dev-itpro/performance/performance-developer)  
