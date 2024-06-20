---
author: brentholtorf
ms.topic: include
ms.date: 03/04/2024
ms.author: bholtorf
ms.service: dynamics-365-business-central
ms.reviewer: bholtorf
---
Hvis selskapet opererer i mer enn ett land eller område, er det sannsynligvis viktig at du kan gjøre forretninger i mer enn én valuta. Du definerer den lokale valutaen på siden **Finansoppsett**. Etterpå vises den lokale valutaen som en tom valuta i dokumenter og transaksjoner. Når **Valuta**-feltet er tomt, er valutaen lokal valuta.

Følgende video forklarer hvordan du konfigurerer lokal valuta.

> [!VIDEO https://www.microsoft.com/videoplayer/embed/RW1iM1n]

Deretter må du definere valutakoder for hver valuta du bruker, hvis du kjøper eller selger i andre valutaer enn den lokale valutaen (LV). Bankkonti kan også opprettes ved hjelp av valutaer. Det er mulig å registrere finanstransaksjoner i ulike valutaer, men finanstransaksjonen vil alltid bokføres i lokal valuta (LV).

[!INCLUDE [finance-currencies-lcy](finance-currencies-lcy-note.md)]

Finans er definert til å bruke den lokale valutaen (LV), men du kan definere at den skal bruke en annen valuta med en valutakurs tilordnet. Når du angir en ny valuta som en tilleggsrapporteringsvaluta, registrerer [!INCLUDE[prod_short](prod_short.md)] beløp automatisk i både lokal valuta og tilleggsrapporteringsvalutaen i alle finansposter og andre poster, for eksempel mva-poster. Hvis du vil ha mer informasjon, se [Sette opp en tilleggsrapporteringsvaluta](../finance-how-setup-additional-currencies.md). Tilleggsrapporteringsvalutaen brukes oftest til å gjøre det enklere å tilrettelegge finansrapportering til eiere som bor i land/områder som bruker andre valutaer enn den lokale valutaen (LV).  

> [!IMPORTANT]
> Hvis du vil bruke en tilleggsrapporteringsvaluta for finansrapportering, må du kontrollere at du har forstått begrensningene. Hvis du vil ha mer informasjon, se [Sette opp en tilleggsrapporteringsvaluta](../finance-how-setup-additional-currencies.md).

> [!NOTE]  
> Når du bokfører i finans med en utenlandsk valuta, konverterer [!INCLUDE [prod_short](prod_short.md)] transaksjonen til lokal valuta ved hjelp av valutakursen for bokføringsdatoen. Finansposten vil ikke inneholde informasjon om hvilken valuta som er brukt, bare verdien i lokal valuta. Hvis du vil holde oversikt over den opprinnelige valutaen, må du bruke salgs- og kjøpsdokumenter i tillegg til bankkontoer som lagrer valutakodeinformasjon for poster.
