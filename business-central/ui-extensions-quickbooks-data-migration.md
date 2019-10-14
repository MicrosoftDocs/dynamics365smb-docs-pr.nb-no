---
title: Bruke QuickBooks Migration-utvidelsen | Microsoft-dokumentasjon
description: Beskriver hvordan du bruker utvidelsen til å importere kunder, leverandører, varer og konti fra QuickBooks Desktop til Business Central.
author: edupont04
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms. search.keywords: app, add-in, manifest, customize, import, implement
ms.date: 10/01/2019
ms.author: edupont
ms.openlocfilehash: 9b5129e4e9ddfe60d969e705d62e023716cde5b6
ms.sourcegitcommit: 02e704bc3e01d62072144919774f1244c42827e4
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 10/01/2019
ms.locfileid: "2311143"
---
# <a name="the-quickbooks-data-migration-extension"></a>Utvidelsen QuickBooks Datamigrering
Denne utvidelsen gjør det enkelt å overføre kunder, leverandører, varer og konti fra QuickBooks til [!INCLUDE[d365fin](includes/d365fin_md.md)]. Hvis virksomheten din bruker QuickBooks i dag, kan du eksportere relevant informasjon og deretter åpner en assistert oppsettsveiledning for å laste opp data til [!INCLUDE[d365fin](includes/d365fin_md.md)].  
Hvis du vil ha mer informasjon, kan du se [Imporere forretningsdata fra andre økonomisystemer](across-import-data-configuration-packages.md).

## <a name="data-from-quickbooks-desktop"></a>Data fra QuickBooks Desktop
 
Du kan importere følgende data fra QuickBooks Online til Business Central:

- Kunder  
- Leverandører  
- Varer  
- Kontoplan  
- Starte saldotransaksjoner i Finans  
- Beholdningsantall for lagervarer  
- Åpne dokumenter for kunder og leverandører, for eksempel fakturaer, kreditnotaer og betalinger  

Vi overfører bare hele beløp på salgs- og kjøpsdokumenter. Vi oppdaterer ikke delvis betalte beløp. Hvis en kunde for eksempel har betalt 300 av totalt 500 kroner på en salgsfaktura, overfører vi hele beløpet på 500. Hvis du har mottatt delbetalinger, må du oppdatere disse manuelt før eller etter at du har overført data. Vi anbefaler at du utligner utestående transaksjoner før du overfører, bare for å gjøre ting enklere senere.

> [!NOTE]
> Vi overfører ikke bestillinger eller ordrer.

## <a name="before-you-start"></a>Før du begynner
En viktig del av overføringen er å angi kontiene som transaksjonene skal overføres til. Det er lurt å planlegge denne tilordningen før du overfører data. Kontiene der du for eksempel bokfører transaksjoner for følgende:

- Salg av varer eller tjenestene til kunder  
- Kjøp av varer eller tjenester fra leverandører  
- Justeringer i Finans  

Business Central krever at det er tilordnet kontonumre til finanskonti. Kontroller at kontonumre er tilordnet til kontiene i QuickBooks.
Hvis transaksjoner i QuickBooks har mva-beløp, må du definere en mva-konto for mva-jurisdiksjonene i Business Central før du kan bokføre transaksjoner.

Du må laste ned Microsofts verktøy for dataeksport for å få dataene dine ut av QuickBooks Desktop-programmet.  Instruksjonene for verktøyet finnes i veiviseren for datamigrering i [!INCLUDE[d365fin](includes/d365fin_md.md)]. Verktøyet vil koble til QuickBooks-programmet ditt og eksportere de aktuelle dataene til en ZIP-fil.  

> [!NOTE]
> For tiden fungerer bare dataeksportverktøyet med QuickBooks 2017 og 2018.

## <a name="finding-the-quickbooks-data-migration-extension"></a>Finne QuickBooks-utvidelse for dataoverføring
Utvidelsen Datamigrering for QuickBooks er installert og klar som en integrert del av den assisterte oppsettsveiledningen for datamigrering. Hvis du er klar til å starte nå og har eksportert dataene dine fra QuickBooks, kan du velge ikonet ![lyspære som åpner Fortell meg-funksjonen](media/ui-search/search_small.png "Fortell hva du vil gjøre") ikonet, angi **Assistert oppsett** og deretter velge den relaterte koblingen. Velg **Overfør forretningsdata**, og følg trinnene i veiledningen.  

## <a name="what-do-i-do-after-i-migrate-data"></a>Hva gjør jeg etter at jeg har overført dataene?
Etter at du har overført dataene, har transaksjoner statusen Ikke bokført, slik at du kan se gjennom dem og foreta justeringer. Hvis du vil se gjennom transaksjonene, går du til siden der de vanligvis er. Hvis du for eksempel vil se gjennom ikke-bokførte salgsfakturaer, går du til siden Salgsfakturaer. Hvis du vil se gjennom utbetalingskladder, går du til siden Utbetalingskladder.
Det finnes et par spesifikke ting du bør gjøre: Hvis transaksjonene i QuickBooks inneholder påslagsbeløp eller rabattbeløp, må du manuelt legge beløpene til de relaterte transaksjonene i Business Central før du bokfører dem.
Hvis du bruker merverdiavgift (mva), må du kanskje legge til en bokføringsgruppe for firma og en varebokføringsgruppe i bokføringsoppsettet, slik at du kan bokføre mva-beløp.
Kontroller startsaldoene for konti i Finans. QuickBooks lagrer ikke gjeldende saldo for alle konti, så du må kanskje rette startsaldoer.

## <a name="see-also"></a>Se også
[Importere forretningsdata fra andre økonomisystemer](across-import-data-configuration-packages.md)  
[Tilpasse [!INCLUDE[d365fin](includes/d365fin_md.md)] ved hjelp av utvidelser](ui-extensions.md)  
