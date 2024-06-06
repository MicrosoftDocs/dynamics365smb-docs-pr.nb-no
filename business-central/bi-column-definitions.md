---
title: Kolonnedefinisjoner i finansrapportering
description: Beskriver hvordan kolonnedefinisjoner i finansrapportering fungerer.
author: kennieNP
ms.author: kepontop
ms.reviewer: bnielse
ms.topic: how-to
ms.date: 03/27/2024
ms.custom: bap-template
ms.search.keywords: 'bi, power BI, analysis, KPI, account schedule, financial report'
ms.search.form: '103, 104, 108, 195, 196, 197, 198, 489, 490, 764, 765, 766'
ms.service: dynamics-365-business-central
---

# <a name="column-definitions-in-financial-reporting"></a>Kolonnedefinisjoner i finansrapportering

Bruk kolonnedefinisjoner til å angi kolonnene som skal inkluderes i en rapport. Du kan for eksempel utforme et rapportoppsett for å sammenligne bevegelse og saldo for samme periode i år og i fjor. Du kan ha opptil 15 kolonner i en kolonnedefinisjon. Flere kolonner er for eksempel nyttig for visning av budsjetter for tolv måneder, med en kolonne som viser totalen.

## <a name="create-or-edit-a-column-definition"></a>Opprett eller rediger en kolonnedefinisjon

Følg denne fremgangsmåten for opprette eller redigere en kolonnedefinisjon.

> [!NOTE]
> En utskriftsversjoner, forhåndsvisningsversjoner og lagrede versjoner av en finansrapport viser maksimalt fem kolonner. Hvis en finansrapporten derimot bare er beregnet for analyse på siden **Finansrapport**, kan du opprette så mange kolonner du vil.

1. På siden for **Finansrapporter** velger du den relevante finansrapporten, og deretter velger du handlingen **Rediger kolonnedefinisjon**.
1. På siden **Kolonnedefinisjon** oppretter du en rad for hver kolonne med finansdata vises etter finansrapporten. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
1. Velg **OK**.
1. Åpne siden **Finansrapport** med jevne mellomrom for å kontrollere at den nye kolonnedefinisjonen fungerer som forventet.

## <a name="built-in-column-definitions"></a>Innebygde kolonnedefinisjoner

[!INCLUDE[prod_short](includes/prod_short.md)] inneholder eksempler på kolonnedefinisjoner som kan hjelpe deg med å komme raskt i gang med å konfigurere finansrapporter som passer dine behov.

<!-- update this when we release the new templates in 24.1
| Column definition code | Description | How to use this column definition | 
| ------------------- | ----------- | ------------------------------ | 
| TBA 1 | TBA 1 | TBA 1 |
| TBA 2 | TBA 2 | TBA 2 |
| TBA 3 | TBA 3 | TBA 3 |
| TBA 4 | TBA 4 | TBA 4 |
-->

## <a name="example-create-a-column-definition-to-calculate-percentages"></a>Eksempel: Opprett en kolonnedefinisjon for å beregne prosentdeler

Du vil da kanskje ta med en kolonne i en finansrapport for å beregne prosentdeler av en sum. Hvis du for eksempel har rader som bryter ned salg etter dimensjon, vil du kanskje ta med en kolonne som angir hvor stor prosentdel av totalt salg i hver rad.

1. Velg ikonet ![Lyspære som åpner funksjonen Fortell meg 2.](media/ui-search/search_small.png "Fortell hva du vil gjøre") og angi **Finansrapporter**, og velg deretter den relaterte koblingen.
1. På siden for **Finansrapporter** velger du en finansrapport.  
1. Velg handlingen **Rediger finansrapport** for å definere en finansrapportrad som skal brukes til å beregne summen prosentene skal baseres på.  
1. Legg til en linje like over den første raden som du vil vise en prosentdel for.  
1. Fyll ut feltene på linjen slik: 
    1. I **Sammentellingstype**-feltet velger du **Angi grunnlag for prosent**. 
    1. Skriv inn en formel for summen som prosentdelen er basert på, i **Sammentelling**-feltet. Hvis rad 11 for eksempel inneholder totalt salg, angir du **11**.  
1. Velg handlingen **Rediger kolonnedefinisjon** for å definere en kolonne.  
1. Fyll ut feltene på linjen slik. 
    1. I **Kolonnetype**-feltet velger du **Formel**. 
    1. Skriv inn en formel for beløpet du vil beregne en prosent for, fulgt av prosenttegnet (%), i **Formel**-feltet. Så hvis kolonnenummeret N inneholder bevegelsen, angir du **N %**.  
1. Gjenta trinn 4 til og med 7 for hver gruppe med rader du vil bryte ned i prosentdeler.

## <a name="comparing-accounting-periods-using-period-formulas"></a>Sammenligne regnskapsperioder ved hjelp av periodeformler

Finansrapporten kan sammenligne resultatene av ulike regnskapsperioder, for eksempel inneværende måned og samme måned i fjor. Dette gjør du ved å åpne **Kolonnedefinisjon**-siden og tilpasse den ved å legge til feltet **Formel - periodesammenligning** som en kolonne. Finn ut mer under [Tilpass arbeidsområdet](ui-personalization-user.md). Deretter kan du sette dette feltet til en periodeformel.  

En regnskapsperiode trenger ikke å samsvare med kalenderen. Regnskapsåret må imidlertid ha samme antall regnskapsperioder, selv om hver periode kan variere i lengde.  

[!INCLUDE[prod_short](includes/prod_short.md)] bruker periodeformelen til å beregne varigheten til sammenligningsperioden, i forhold til perioden som er angitt i datofilteret i rapporten. Sammenligningsperioden er basert på perioden for startdatoen i datofilteret. Tabellen nedenfor viser forkortelsene for periodespesifikasjoner.

| Forkortelse | Description                                                                           |
| ------------ | ------------------------------------------------------------------------------------- |
| P            | Periode.                                                                                |
| SP           | Siste periode av et regnskapsår, et halvår eller kvartal.                                   |
| HP           | Inneværende periode av et regnskapsår, et halvår eller kvartal. Bruk IP i formlar for å oppgi perioden som skal starte eller avslutte formelen. For eksempel angir RÅ\[1.. IP\] tiden fra begynnelsen av gjeldende regnskapsår til gjeldende periode.|
| RÅ           | Regnskapsår. Eksempelvis viser RÅ\[1..3\] det første kvartal av inneværende regnskapsår. |

Eksempler på formler:

| Formel | Description |
|-----|-----|
| \<Blank\>       | Inneværende periode. |
| \-1P            | Forrige periode.            |
| \-1RÅ\[1..SP\]  | Hele forrige regnskapsår.                  |
| \-1RÅ           | Inneværende periode i forrige regnskapsår.       |
| \-1RÅ\[1..3\]   | Første kvartal av forrige regnskapsår.        |
| \-1RÅ\[1..IP\]  | Fra begynnelsen av forrige regnskapsår til og med inneværende periode i forrige regnskapsår, inkludert begge perioder. |
| \-1RÅ\[IP..SP\] | Fra inneværende periode i forrige regnskapsår til siste periode i forrige regnskapsår, inkludert begge perioder.   |

Hvis du vil beregne etter regelmessige perioder, angir du en formel i feltet **Datoformel – sammenligning** i stedet. Hvis feltet for eksempel er satt til –1Å, foretar [!INCLUDE [prod_short](includes/prod_short.md)] en sammenligning med samme periode ett år tidligere.

> [!NOTE]
> Det er ikke alltid tydelig hvilke perioder du sammenligner, siden du kan angi et datofilter i en rapport som inneholder andre datoer enn regnskapsperiodene som gjenspeiles i kontoplanen. Hvis du oppretter en finansrapport der du vil sammenligne denne perioden med samme periode i fjor, setter du **Datoformel – sammenligning**-feltet til **–1RÅ**. Deretter kjører du rapporten **28. februar** og setter datofilteret til **januar og februar**. Dermed sammenligner finansrapport januar og februar i år med januar i fjor, som er den eneste fullførte regnskapsperioden av de to for forrige år.  

Lær mer på [Arbeid med kalenderdatoer og klokkeslett](ui-enter-date-ranges.md).

[!INCLUDE [report-best-practices-column-defs](includes/report-best-practices-column-defs.md)]

## <a name="import-or-export-financial-report-column-definitions"></a>Importer eller eksporter av kolonnedefinisjoner for finansrapport

Fra og med lanseringsbølge 1 i 2024 (versjon 24.1) kan du importere og eksportere kolonnedefinisjoner for finansrapporter som RapidStart-konfigurasjonspakker. Konfigurasjonspakker er for eksempel nyttig for deling av informasjon med andre selskaper. Pakken opprettes i en .rapidstart-fil, som komprimerer innholdet.

> [!NOTE]
> Når du importerer kolonnedefinisjoner for finansrapport, blir eksisterende poster med samme navn som de du importerer, erstattet med de nye definisjonene. Konfigurasjonspakken for en rapportdefinisjon overskriver ikke eksisterende rad- eller kolonnedefinisjoner som brukes i rapportdefinisjonen.

Hvis du vil importere eller eksportere kolonnedefinisjoner for finansrapport, gjør du følgende:

1. Velg ikonet ![Lyspære som åpner funksjonen Fortell meg 4.](media/ui-search/search_small.png "Fortell hva du vil gjøre") og angi **Kolonnedefinisjoner**, og velg deretter den relaterte koblingen.
1. Velg raddefinisjonen, og velg deretter **Importer kolonnedefinisjon** eller **Eksporter kolonnedefinisjon**, avhengig av hva du vil gjøre.

## <a name="see-also"></a>Se også

[Raddefinisjoner i finansrapportering](bi-row-definitions.md)  
[Klargjør finansrapportering](bi-how-work-account-schedule.md)  
[Finansforretningsanalyse](bi.md)  
[Finans](finance.md)  
[Konfigurere finans](finance-setup-finance.md)  
[Arbeid med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
