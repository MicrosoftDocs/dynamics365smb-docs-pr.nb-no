---
title: Kombinere leveringer på én faktura | Microsoft-dokumentasjon
description: Hvis du vil fakturere mer enn én følgeseddel av gangen, kan du bruke funksjonen for samling av følgesedler.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: 757f7cd38a6325df0e8dc0d283d58c42a8ab823e
ms.sourcegitcommit: 2e7307fbe1eb3b34d0ad9356226a19409054a402
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 12/17/2020
ms.locfileid: "4748271"
---
# <a name="combine-shipments-on-a-single-invoice"></a>Kombinere leveringer på én faktura
Hvis du vil fakturere mer enn én følgeseddel av gangen, kan du bruke funksjonen for samling av følgesedler.  

Før du kan opprette samlefakturaer, må du bokføre mer enn én følgeseddel for den samme kunden i én og samme valuta. Du må med andre ord opprette minst to ordrer og bokføre disse ordrene som levert, men ikke fakturert. 

## <a name="to-manually-combine-shipments-on-a-single-invoice"></a>Kombinere leveringer på én faktura manuelt  
1. Velg ikonet ![Lyspære som åpner Fortell meg-funksjonen](media/ui-search/search_small.png "Fortell hva du vil gjøre"), angi **Salgsfakturaer**, og velg deretter den relaterte koblingen.  
2. Velg handlingen **Ny**. Hvis du vil ha mer informasjon, kan du se [Fakturere salg](sales-how-invoice-sales.md).
3. I feltet **Salg til-kundenr.** angir du kunden som skal motta fakturaen for de leverte varene.  
4. På hurtigfanen **Linjer** velger du handlingen **Hent leveringslinjer**.  
5. Velg følgeseddellinjen du vil inkludere i fakturaen:  

    - Du setter inn alle linjene ved å merke dem og velge **OK**.  
    - Du setter inn bestemte linjer ved å merke dem og velge **OK**. Du kan bruke CTRL-tasten for å velge flere linjer som ikke ligger inntil hverandre.  

    Hvis du valgte en feil følgeseddellinje, eller du vil starte på nytt, kan du ganske enkelt slette linjene på fakturaen og kjøre funksjonen **Hent følgeseddellinjer** på nytt.  
7. Velg handlingen **Bokfør** for å bokføre fakturaen.  

## <a name="to-automatically-combine-shipments-on-a-single-invoice"></a>Slik kombinerer du leveringer på én enkelt faktura automatisk:  
[!INCLUDE[prod_short](includes/prod_short.md)] velger bare ordrer der **Opprett samlefaktura** er valgt. 

1. Velg ikonet ![Lyspære som åpner Fortell meg-funksjonen](media/ui-search/search_small.png "Fortell hva du vil gjøre"), angi **Opprett samlefaktura**, og velg deretter den relaterte koblingen. Forespørselen for satsvis jobb åpnes.  
2. Fyll ut feltene etter behov. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
3. Merk av for **Bokfør fakturaer**.  
4. Velg **OK**-knappen.  

> [!NOTE]  
>  Du må bokføre fakturaene manuelt hvis det ikke var merket av for alternativet **Bokfør fakturaer** for kjørselen.  

## <a name="to-remove-open-sales-orders-after-combined-shipment-posting"></a>Fjerne åpne ordrer etter kombinert leveringsbokføring 
Når du oppretter og bokfører en samlefaktura, opprettes en bokført salgsfaktura for fakturalinjene. **Fakturert (antall)**-feltet på den opprinnelige rammeordren eller ordren oppdateres ut fra det fakturerte antallet.  

Når du fakturerer følgesedler på denne måten, eksisterer fortsatt ordrene som følgesedlene ble bokført fra, selv om de er fullstendig levert og fakturert.   

1. Velg ikonet ![Lyspære som åpner Fortell meg-funksjonen](media/ui-search/search_small.png "Fortell hva du vil gjøre"), angi **Slett fakturerte ordrer**, og velg deretter den relaterte koblingen.  
2. Angi hvilke ordrer som skal slettes, i **Nr.** -filterfeltet.  
3. Velg **OK**-knappen.  

Du kan også slette individuelle ordrer manuelt.  

Gjenta trinn 1 til 3 for eventuelle andre berørte dokumenter, for eksempel ordrer.

## <a name="see-also"></a>Se også  
[Salg](sales-manage-sales.md)  
[Arbeide med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)
