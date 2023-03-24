---
author: edupont04
ms.topic: include
ms.date: 03/15/2022
ms.author: edupont
---
Ettersom selskaper har drift i stadig flere land/regioner, blir det viktigere at de kan handle og rapportere finansinformasjon i mer enn én valuta. Den lokale valutaen (LV) er definert på siden **Finansoppsett** som beskrevet i artikkelen [Forstå finans og kontoplanen](../finance-general-ledger.md). Når den lokale valutaen (LV) er definert, vises den som en tom valuta, så når feltet **Valuta** er tomt, betyr det at valutaen er i LV.  

Deretter må du definere valutakoder for hver valuta du bruker, hvis du kjøper eller selger i andre valutaer enn den lokale valutaen (LV). Bankkonti kan også opprettes ved hjelp av valutaer. Det er mulig å registrere finanstransaksjoner i ulike valutaer, men finanstransaksjonen vil alltid bokføres i lokal valuta (LV).

[!INCLUDE [finance-currencies-lcy](finance-currencies-lcy-note.md)]

Finans er definert til å bruke den lokale valutaen (LV), men du kan definere at den skal bruke en annen valuta med en valutakurs tilordnet. Når du angir en ny valuta som en såkalt tilleggsrapporteringsvaluta, registrerer [!INCLUDE[prod_short](prod_short.md)] beløp automatisk i både LV og denne tilleggsrapporteringsvalutaen i alle finansposter og andre poster, for eksempel mva-poster. Hvis du vil ha mer informasjon, se [Sette opp en tilleggsrapporteringsvaluta](../finance-how-setup-additional-currencies.md). Tilleggsrapporteringsvalutaen brukes oftest til å gjøre det enklere å tilrettelegge finansrapportering til eiere som bor i land/områder som bruker andre valutaer enn den lokale valutaen (LV).  

> [!IMPORTANT]
> Hvis du vil bruke en tilleggsrapporteringsvaluta for finansrapportering, må du kontrollere at du har forstått begrensningene. Hvis du vil ha mer informasjon, se [Sette opp en tilleggsrapporteringsvaluta](../finance-how-setup-additional-currencies.md).

> [!NOTE]  
> Når du bokfører i finans ved hjelp av en valutakode, for eksempel for å bokføre en utgift i en finanskladd ved hjelp av en valutakode, omregnes transaksjonen til LV ved hjelp av valutakursen for bokføringsdatoen. Finansposten vil ikke inneholde informasjon om hvilken valuta som er brukt, bare verdien i LV. Hvis du vil holde oversikt over den opprinnelige valutaen, for eksempel for en faktura, må du bruke salgs- og kjøpsdokumenter i tillegg til bankkontoer som lagrer valutakodeinformasjon for postene.
