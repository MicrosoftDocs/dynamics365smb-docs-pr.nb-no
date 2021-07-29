---
title: Vis Tabellinformasjon
description: Lær hvordan du kan vise informasjon om databasetabellene rett fra klientgrensesnittet i Business Central.
author: jswymer
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.date: 06/14/2021
ms.author: jswymer
ms.openlocfilehash: 581d92010fa566c33775ffd6238ca6e0cfca0837
ms.sourcegitcommit: a7cb0be8eae6ece95f5259d7de7a48b385c9cfeb
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 07/08/2021
ms.locfileid: "6443082"
---
# <a name="viewing-table-information"></a>Vise Tabellinformasjon

Siden **Informasjon om 8700-tabellen** inneholder informasjon om alle system- og forretningstabeller i en Business Central-løsning. Siden viser spesielt informasjon om mengden data som tabellene inneholder.

Denne informasjonen er nyttig for å feilsøke ytelsesproblemer, siden dette gir deg muligheten til å se fordelingen av datastørrelsen på tvers av tabeller.

## <a name="viewing-table-information"></a>Vise tabellinformasjon

Du kan åpne denne siden ved å velge ikonet ![Søk etter side eller rapport.](media/ui-search/search_small.png "Ikonet Søk etter side eller rapport") og angi **Tabellinformasjon**, og velg deretter den relaterte koblingen.

Følgende tabell beskriver opplysningene som er gitt for hver tabell:

|Kolonne|Beskrivelse|
|------|-----------|
|Selskapsnavn|Navnet på selskapet (hvis noen) som tabellen tilhører.|
|Tabellnavn|Navnet på tabellen.|
|Tabellnr.|ID-en for tabellen|
|Antall poster|Totalt antall poster lagret i tabellen.|
|Poststørrelse|Gjennomsnittlig poststørrelse i kB/post. Verdien beregnes ved hjelp av følgende formel: 1024 (størrelse)/(antall poster). |

## <a name="see-also"></a>Se også

[Kontrollere sider](across-inspect-page.md)  
[Ytelsesartikler for utviklere](/dynamics365/business-central/dev-itpro/performance/performance-developer)  


[!INCLUDE[footer-include](includes/footer-banner.md)]