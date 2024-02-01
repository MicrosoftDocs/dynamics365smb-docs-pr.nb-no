---
title: Utvidelsen for feilsøking av aktivaposter
description: Det er enklere å arbeide med hele tall. Bruk denne utvidelsen til å runde av beløp for aktiva i aktivaposten.
documentationcenter: ''
author: brentholtorf
ms.topic: conceptual
ms.devlang: al
ms.search.keywords: 'machinery, buildings'
ms.date: 10/01/2021
ms.author: bholtorf
ms.service: dynamics-365-business-central
---
# <a name="the-troubleshooting-fa-ledger-entries-extension"></a>Utvidelsen for feilsøking av aktivaposter
Bruk utvidelsen for feilsøking av aktivaposter til å runde av avskrivnings- og anskaffelsesbeløp i aktivaposter til hele numre. Du kan for eksempel avrunde et beløp på 30 000,44 til 30 000. Vanlige årsaker til avrundingsfeil er dataoverføring, plutselig bokføring av beløp i finans, eller tilpasninger du har gjort i [!INCLUDE[prod_short](includes/prod_short.md)].

Utvidelsen for feilsøking av aktivaposter er forhåndsinstallert og klar til bruk. Hvis du fjerner utvidelsen, men vil installere den på nytt, finner du den i AppSource.

## <a name="troubleshooting-fixed-asset-ledger-entries"></a>Feilsøking av aktivaposter
Når du åpner siden **Aktivakort** for første gang, er det planlagt at prosjektkøposten **Skanning av aktivaposter** skal overvåke beløp hver søndag. Hvis det blir funnet beløp som du kanskje vil avrunde, vises det en melding neste gang du åpner Aktivakort-siden. Varselet gir et **Se mer**-alternativ som åpner siden **Aktivaposter med avrundingsproblemer**, som viser postene med beløp som du kanskje vil avrunde. Hvis du vil avrunde beløpene, velger du postene og velger deretter **Godta utvalg**-handlingen. Du kan bruke handlingen **Søk etter poster med problemer** til å oppdatere oversikten med nye problemer som har oppstått etter at prosjektkjøposten ble kjørt forrige søndag.

## <a name="see-also"></a>Se også
[Aktiva](fa-manage.md)  
[Administrer aktiva](fa-manage.md)  
[Vedlikehold aktiva](fa-how-maintain.md)  
[Tilpassing av Business Central Online med utvidelser](ui-extensions.md)  
[Finans](finance.md)  
[Bli klar til å gjøre forretninger](ui-get-ready-business.md)  
[Arbeide med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]



