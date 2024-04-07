---
title: Kombinere leveringer på én faktura | Microsoft-dokumentasjon
description: 'Hvis du vil fakturere mer enn én følgeseddel av gangen, kan du bruke funksjonen for samling av følgesedler.'
author: brentholtorf
ms.topic: conceptual
ms.devlang: al
ms.search.keywords: null
ms.date: 12/16/2021
ms.author: bholtorf
ms.service: dynamics-365-business-central
---
# Kombinere leveringer på én faktura

Hvis du vil fakturere mer enn én følgeseddel av gangen, kan du bruke funksjonen for samling av følgesedler.  

Før du kan opprette samlefakturaer, må du bokføre mer enn én følgeseddel for den samme kunden i én og samme valuta. Du må med andre ord opprette minst to ordrer og bokføre disse ordrene som levert, men ikke fakturert. 

## Kombinere leveringer på én faktura manuelt

1. Velg ikonet ![Lyspære som åpner funksjonen Fortell meg.](media/ui-search/search_small.png "Fortell hva du vil gjøre") og skriv inn **Salgsfakturaer**, og velg deretter den relaterte koblingen.  
2. Velg handlingen **Ny**. Hvis du vil ha mer informasjon, kan du se [Fakturere salg](sales-how-invoice-sales.md).
3. I feltet **Salg til-kundenr.** angir du kunden som skal motta fakturaen for de leverte varene.  
4. På hurtigfanen **Linjer** velger du handlingen **Hent leveringslinjer**.  
5. Velg følgeseddellinjen du vil inkludere i fakturaen:  

    - Du setter inn alle linjene ved å merke dem og velge **OK**.  
    - Du setter inn bestemte linjer ved å merke dem og velge **OK**. Du kan bruke CTRL-tasten for å velge flere linjer som ikke ligger inntil hverandre.  

    Hvis du valgte en feil følgeseddellinje, eller du vil starte på nytt, kan du ganske enkelt slette linjene på fakturaen og kjøre funksjonen **Hent følgeseddellinjer** på nytt.  
7. Velg handlingen **Bokfør** for å bokføre fakturaen.  

> [!TIP]  
> Hvis du har levert ordrer der feltet **Salg til-kundenr.** er forskjellig fra **Faktura til-kundenr.**, vises ikke disse linjene i rapporten **Hent følgeseddellinjer**. Bruk tilpassing hvis du vil legge til feltet **Salg til-kunde** på siden og fjerne filteret. Nå kan du legge til leveringslinjer i fakturaen uavhengig av verdien i feltet **Salg til-kundenr.**, så lenge feltet **Faktura til-kundenr.** på leveringslinjene samsvarer med verdien på salgsfakturaen.  

## Slik kombinerer du leveringer på én enkelt faktura automatisk:

[!INCLUDE[prod_short](includes/prod_short.md)] velger bare ordrer der **Opprett samlefaktura** er valgt. 

1. Velg ikonet ![Lyspære som åpner funksjonen Fortell meg.](media/ui-search/search_small.png "Fortell hva du vil gjøre") og angi **Kombiner leveringer**, og velg deretter den relaterte koblingen. Forespørselen for satsvis jobb åpnes.  
2. Fyll ut feltene etter behov. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
3. Merk av for **Bokfør fakturaer**.  
4. Velg **OK**-knappen.  

> [!NOTE]  
>  Du må bokføre fakturaene manuelt hvis det ikke var merket av for alternativet **Bokfør fakturaer** for kjørselen.  

## Fjerne åpne ordrer etter kombinert leveringsbokføring

Når du oppretter og bokfører en samlefaktura, opprettes en bokført salgsfaktura for fakturalinjene. **Fakturert (antall)**-feltet på den opprinnelige rammeordren eller ordren oppdateres ut fra det fakturerte antallet.  

Når du fakturerer følgesedler på denne måten, eksisterer fortsatt ordrene som følgesedlene ble bokført fra, selv om de er fullstendig levert og fakturert.   

1. Velg ikonet ![Lyspære som åpner funksjonen Fortell meg.](media/ui-search/search_small.png "Fortell hva du vil gjøre") og angi **Slett fakturerte ordrer**, og velg deretter den relaterte koblingen.  
2. Angi hvilke ordrer som skal slettes, i **Nr.** -filterfeltet.  
3. Velg **OK**-knappen.  

Du kan også slette individuelle ordrer manuelt.  

Gjenta trinn 1 til 3 for eventuelle andre berørte dokumenter, for eksempel ordrer.

## Se også

[Salg](sales-manage-sales.md)  
[Arbeid med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]
