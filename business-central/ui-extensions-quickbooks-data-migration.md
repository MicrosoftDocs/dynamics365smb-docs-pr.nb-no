---
title: Utvidelsen QuickBooks Datamigrering
description: Beskriver hvordan du bruker utvidelsen til å importere kunder, leverandører, varer og konti fra QuickBooks Desktop til Business Central.
author: edupont04
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms. search.keywords: app, add-in, manifest, customize, import, implement
ms.date: 06/24/2021
ms.author: edupont
ms.openlocfilehash: 5c910aa7ab769af315c34db27c065fb8b496c878
ms.sourcegitcommit: ef80c461713fff1a75998766e7a4ed3a7c6121d0
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 02/15/2022
ms.locfileid: "8136746"
---
# <a name="the-quickbooks-data-migration-extension"></a>Utvidelsen QuickBooks Datamigrering

Denne utvidelsen gjør det enkelt å overføre kunder, leverandører, varer og konti fra QuickBooks til [!INCLUDE[prod_short](includes/prod_short.md)]. Hvis virksomheten din bruker QuickBooks i dag, kan du eksportere relevant informasjon og deretter åpner en assistert oppsettsveiledning for å laste opp data til [!INCLUDE[prod_short](includes/prod_short.md)].  
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

Du må laste ned Microsofts verktøy for dataeksport for å få dataene dine ut av QuickBooks Desktop-programmet.  Instruksjonene for verktøyet finnes i veiviseren for datamigrering i [!INCLUDE[prod_short](includes/prod_short.md)]. Verktøyet vil koble til QuickBooks-programmet ditt og eksportere de aktuelle dataene til en ZIP-fil.  

> [!NOTE]
> For tiden fungerer bare dataeksportverktøyet med QuickBooks 2017 og 2018.

## <a name="finding-the-quickbooks-data-migration-extension"></a>Finne QuickBooks-utvidelse for dataoverføring

Utvidelsen Datamigrering for QuickBooks er installert og klar som en integrert del av den assisterte oppsettsveiledningen for datamigrering. Hvis du er klar til å komme i gang nå og har eksporter dataene fra QuickBooks, velger du ikonet ![Lyspæren som åpner funksjonen Fortell meg.](media/ui-search/search_small.png "Fortell hva du vil gjøre") og angir **Assistert oppsett** og velger den relaterte koblingen. Velg **Overfør forretningsdata**, og følg trinnene i veiledningen.  

## <a name="what-do-i-do-after-i-migrate-data"></a>Hva gjør jeg etter at jeg har overført dataene?

Etter at du har overført dataene, har transaksjoner statusen Ikke bokført, slik at du kan se gjennom dem og foreta justeringer. Hvis du vil se gjennom transaksjonene, går du til siden der de vanligvis er. Hvis du for eksempel vil se gjennom ikke-bokførte salgsfakturaer, går du til siden Salgsfakturaer. Hvis du vil se gjennom utbetalingskladder, går du til siden Utbetalingskladder.
Det finnes et par spesifikke ting du bør gjøre: Hvis transaksjonene i QuickBooks inneholder påslagsbeløp eller rabattbeløp, må du manuelt legge beløpene til de relaterte transaksjonene i Business Central før du bokfører dem.
Hvis du bruker merverdiavgift (mva), må du kanskje legge til en bokføringsgruppe for firma og en varebokføringsgruppe i bokføringsoppsettet, slik at du kan bokføre mva-beløp.
Kontroller startsaldoene for konti i Finans. QuickBooks lagrer ikke gjeldende saldo for alle konti, så du må kanskje rette startsaldoer.

## <a name="see-also"></a>Se også

[Importere forretningsdata fra andre økonomisystemer](across-import-data-configuration-packages.md)  
[Tilpasse [!INCLUDE[prod_short](includes/prod_short.md)] ved hjelp av utvidelser](ui-extensions.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]