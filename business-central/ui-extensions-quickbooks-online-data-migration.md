---
title: Utvidelsen QuickBooks Online-datamigrering
description: 'Beskriver hvordan du bruker utvidelsen til å overføre kunder, leverandører, varer og konti fra QuickBooks Online til Business Central.'
author: brentholtorf
ms.topic: conceptual
ms.devlang: al
ms.search.keywords: 'extension, migrate, data, QuickBooks, import'
ms.search.form: '1830,'
ms.date: 06/24/2021
ms.author: bholtorf
ms.service: dynamics-365-business-central
---

# <a name="the-quickbooks-online-data-migration-extension"></a>Utvidelsen QuickBooks Online-datamigrering

Utvidelsen er inkludert i den assisterte oppsettsveiledningen **Datamigrering** for å hjelpe deg å overføre viktige forretningsdata fra QuickBooks Online til [!INCLUDE[prod_short](includes/prod_short.md)]. Dette er for eksempel praktisk når virksomheten er i vekst og du har besluttet å oppgradere appen for forretningsdrift ved å begynne å bruke [!INCLUDE[prod_short](includes/prod_short.md)].

## <a name="what-data-can-i-import-from-quickbooks-online"></a>Hvilke data kan jeg importere fra QuickBooks Online?

Du kan importere følgende data fra QuickBooks Online til [!INCLUDE[prod_short](includes/prod_short.md)]:  

* Kunder
* Leverandører
* Varer
* Kontoplan
* Startsaldotransaksjon i Finans
* Beholdningsantall for lagervarer
* Åpne dokumenter for kunder og leverandører, for eksempel fakturaer, kreditnotaer og betalinger

Vi overfører bare hele beløp på salgs- og kjøpsdokumenter. Vi oppdaterer ikke delvis betalte beløp. Hvis en kunde for eksempel har betalt 300 av totalt 500 kroner på en salgsfaktura, overfører vi hele beløpet på 500. Hvis du har mottatt delbetalinger, må du oppdatere disse manuelt før eller etter at du har overført data. Vi anbefaler at du utligner utestående transaksjoner før du overfører, bare for å gjøre ting enklere senere.

> [!NOTE]  
> Vi overfører ikke bestillinger eller ordrer.

## <a name="before-you-start"></a>Før du begynner

En viktig del av overføringen er å angi kontiene som transaksjonene skal overføres til. Det er lurt å planlegge denne tilordningen før du overfører data. Kontiene der du for eksempel bokfører transaksjoner for følgende:  

* Salg av varer eller tjenestene til kunder.
* Kjøp av varer eller tjenester fra leverandører.  
* Justeringer i Finans.  

[!INCLUDE[prod_short](includes/prod_short.md)] krever at det er tilordnet kontonumre til finanskonti. Kontroller at kontonumre er tilordnet til kontiene i QuickBooks Online.

Hvis transaksjoner i QuickBooks Online har mva-beløp, må du definere en mva-konto for mva-jurisdiksjonene i [!INCLUDE[prod_short](includes/prod_short.md)] før du kan bokføre transaksjoner.

## <a name="how-do-i-start-using-the-extension"></a>Hvordan begynner jeg å bruke utvidelsen?

Det er enkelt å komme i gang. Alt du trenger å gjøre, er å kjøre den assisterte oppsettsveiledningen **Datamigrering**. Slik gjør du det:

1. Velg ikonet ![Lyspære som åpner funksjonen Fortell meg.](media/ui-search/search_small.png "Fortell hva du vil gjøre") og angi **Assistert oppsett**, og velg deretter **Overfør forretningsdata**.
2. Følg instruksjonene for hvert trinn i den assisterte oppsettsveiledningen.

## <a name="what-do-i-do-after-i-migrate-data"></a>Hva gjør jeg etter at jeg har overført dataene?

Etter at du har overført dataene, har transaksjoner statusen **Ikke bokført**, slik at du kan se gjennom dem og foreta justeringer. Hvis du vil se gjennom transaksjonene, går du til siden der de vanligvis er. Hvis du for eksempel vil se gjennom ikke-bokførte salgsfakturaer, går du til siden **Salgsfakturaer**. Hvis du vil se gjennom utbetalingskladder, går du til siden **Utbetalingskladder**.  

Det er enkelte bestemte ting du bør gjøre:

* Hvis transaksjonene i QuickBooks Online hadde påslags- eller rabattbeløp, må du legge til beløpene manuelt i de relaterte transaksjonene i [!INCLUDE[prod_short](includes/prod_short.md)] før du bokfører dem.
* Hvis du bruker merverdiavgift (mva), må du kanskje legge til en bokføringsgruppe for firma og en varebokføringsgruppe i bokføringsoppsettet, slik at du kan bokføre mva-beløp.
* Kontroller startsaldoene for konti i Finans. QuickBooks Online lagrer ikke gjeldende saldo for alle konti, så du må kanskje rette startsaldoer.

## <a name="see-also"></a>Se også

[Importer forretningsdata fra andre økonomisystemer](across-import-data-configuration-packages.md)  
[Tilpass [!INCLUDE[prod_short](includes/prod_short.md)] ved hjelp av utvidelser](ui-extensions.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
