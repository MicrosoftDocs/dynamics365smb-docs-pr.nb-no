---
title: Angre monteringsbokføring
description: Finn ut hvordan du korrigerer feil i en bokført monteringsordre.
author: brentholtorf
ms.author: bholtorf
ms.reviewer: andreipa
ms.topic: how-to
ms.date: 02/21/2023
ms.custom: bap-template
ms.search.keywords: 'kit, kitting'
ms.search.form: '900, 901, 902, 903, 904, 907, 910, 916, 920, 921, 922, 923, 940, 941, 942, 930, 931, 932, 914, 915, 905'
---
# Angre monteringsbokføring

Angre bokføringen av en monteringsordre for å korrigere en feil eller fjerne en uønsket bokføring.

Når du angrer en bokført monteringsordre, blir det opprettet korrigerende vareposter for å tilbakeføre de opprinnelige postene. Hver positive avgangspost for monteringsvaren tilbakeføres ved en negativ avgangspost. Hver negative forbrukspost for en monteringskomponent tilbakeføres ved en positiv forbrukspost. Utligning av fast kostnad opprettes automatisk mellom korrigerende og originale poster for å sikre nøyaktig tilbakeføring av kostnad.  

Når du angrer en fullstendig bokført monteringsordre, kan du gjenopprette den opprinnelige ordren. Hvis du for eksempel vil gjøre korrigeringer før du bokfører den igjen.  

Når du angrer en delvis bokført monteringsordre, vil alle berørte antallsfelt, for eksempel feltene **Montert antall**, **Forbrukt antall** og **Restantall**, bli gjenopprettet til verdiene de hadde før bokføringen.  

Hvis du vil opprette på nytt eller gjenopprette monteringsordrer, må vare i opprinnelig bokføring oppfylle følgende betingelser:  

* Det er fortsatt på lager. Det vil si ikke solgt eller på annen måte forbrukt gjennom utgående transaksjoner.  
* Den er ikke reservert.  
* Den er i hyllen som den ble lagt i.  

Monteringsordrer kan bare gjenopprettes hvis antallet og rekkefølgen til linjene i den opprinnelige monteringsordren ikke endres.  

> [!TIP]  
> Du kan løse konflikter som skyldes endringer i linjene, ved å tilbakestille endringene på de aktuelle linjene manuelt, før du angrer den tilknyttede bokførte monteringsordren. Du kan også bokføre monteringsordren fullstendig og deretter opprette den på nytt når du angrer bokføringen.  

Fremgangsmåten nedenfor beskriver hvordan du angrer bokførte monteringsordrer som inneholder varene som ble montert til lager. Hvis du vil angre bokførte monteringsordrer med varer som er montert-til-ordre, bruker du **Angre levering**-handlingen på den tilhørende bokførte leveringen. Hvis du vil finne ut mer om å angre leveringer, går du til [Tilbakefør kladdebokføringer og angre mottak/leveringer](finance-how-reverse-journal-posting.md). Angring av bokførte monteringsordre skjer automatisk på samme måte som beskrevet i artikkelen.  

## Slik angrer du bokføringen av en monteringsordre:

Du kan angre fullstendig eller delvis bokførte monteringsordrer.

1. Velg ikonet ![Lyspære som åpner funksjonen Fortell meg.](media/ui-search/search_small.png "Fortell hva du vil gjøre") og skriver inn **Bokførte monteringsordrer** og velger den relaterte koblingen.  

   Hver delvise bokføring oppretter en separat bokført monteringsordre.  
2. Åpne den bokførte monteringsordren du vil angre, og velg deretter **Angre montering**.  

    Hvis den bokførte monteringsordren er knyttet til en fullstendig bokført monteringsordre som er slettet, kan du opprette på nytt og deretter slette ordren. Du kan for eksempel gjenopprette ordren fordi du vil behandle den på nytt.  
3. Hvis du vil gjenopprette monteringsordren, velger du **Ja**. Hvis du vil angre bokføringen uten å opprette monteringsordren på nytt, velger du **Nei**.  

Feltet **Tilbakeført** i monteringsordre endres til **Ja**. Bokføringen av monteringsordren er nå tilbakeført. Du kan behandle hele monteringsordren hvis du velger å gjenopprette den, eller den åpne monteringsordren du har gjenopprettet til den opprinnelige tilstanden.  

> [!NOTE]  
> Hvis du vil gjenopprette antallene fra flere delvise bokføringer i en monteringsordre, må du angre alle bokførte monteringsordrer ved å følge trinn 1 til 3.  

## Se også

[Monteringsstyring](assembly-assemble-items.md)  
[Tilbakefør kladdebokføringer og angre mottak/leveringer](finance-how-reverse-journal-posting.md)  
[Behandle ordrereturer eller annulleringer](sales-how-process-sales-returns-cancellations.md)  
[Arbeid med monteringsstykklister](assembly-how-work-assembly-boms.md)  
[Lager](inventory-manage-inventory.md)  
[Oversikt over lagerstyring](design-details-warehouse-management.md)
[Arbeid med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]