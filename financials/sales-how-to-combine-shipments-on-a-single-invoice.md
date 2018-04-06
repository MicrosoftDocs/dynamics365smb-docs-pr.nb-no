---
title: "Kombinere leveringer på én faktura | Microsoft-dokumentasjon"
description: "Hvis du vil fakturere mer enn én følgeseddel av gangen, kan du bruke funksjonen for samling av følgesedler."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 08/14/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: bec0619be0a65e3625759e13d2866ac615d7513c
ms.openlocfilehash: c9f2464014f2078f2a86f2e7d8a72873fa4015a8
ms.contentlocale: nb-no
ms.lasthandoff: 03/22/2018

---
# <a name="combine-shipments-on-a-single-invoice"></a>Kombinere leveringer på én faktura
Hvis du vil fakturere mer enn én følgeseddel av gangen, kan du bruke funksjonen for samling av følgesedler.  

 Før du kan opprette samlefakturaer, må du bokføre mer enn én følgeseddel for den samme kunden i én og samme valuta. Du må med andre ord ha fylt ut minst to ordrer og bokført disse ordrene som levert, men ikke fakturert. Du kombinerer forsendelser ved å merke av for **Opprett samlefaktura** på hurtigfanen **Levering** på **kundekortet**.  

## <a name="to-manually-combine-shipments-on-a-single-invoice"></a>Kombinere leveringer på én faktura manuelt  
1. Velg ikonet ![Søk etter side eller rapport](media/ui-search/search_small.png "Søk etter side eller rapport"), angi **Salgsfakturaer**, og velg deretter den relaterte koblingen.  
2. Velg handlingen **Ny**. Hvis du vil ha mer informasjon, kan du se [Fakturere salg](sales-how-invoice-sales.md).
3. I feltet **Salg til-kundenr.** angir du kunden som skal motta fakturaen for de leverte varene.  
4. På hurtigfanen **Linjer** velger du handlingen **Hent leveringslinjer**.  
5. Velg følgeseddellinjen du vil inkludere i fakturaen:  

    - Du setter inn alle linjene ved å merke dem og velge **OK**.  
    - Du setter inn bestemte linjer ved å merke dem og velge **OK**. Du kan bruke CTRL-tasten for å velge flere linjer som ikke ligger inntil hverandre.  

    Hvis du valgte en feil følgeseddellinje, eller du vil starte på nytt, kan du ganske enkelt slette linjene på fakturaen og kjøre funksjonen **Hent følgeseddellinjer** på nytt.  
7. Velg handlingen **Bokfør** for å bokføre fakturaen.  

## <a name="to-automatically-combine-shipments-on-a-single-invoice"></a>Slik kombinerer du leveringer på én enkelt faktura automatisk:  
1. Velg ikonet ![Søk etter side eller rapport](media/ui-search/search_small.png "Søk etter side eller rapport"), angi **Opprett samlefaktura**, og velg deretter den relaterte koblingen. Vinduet for kjørselforespørsel åpnes.  
2. Fyll ut feltene etter behov. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
3. Merk av for **Bokfør fakturaer**.  
4.  Velg **OK**.  

> [!NOTE]  
>  Du må bokføre fakturaene manuelt hvis det ikke var merket av for alternativet **Bokfør fakturaer** for kjørselen.  

## <a name="to-remove-open-sales-orders-after-combined-shipment-posting"></a>Fjerne åpne ordrer etter kombinert leveringsbokføring 
Når du oppretter og bokfører en samlefaktura, opprettes en bokført salgsfaktura for fakturalinjene. **Fakturert (antall)**-feltet på den opprinnelige rammeordren eller ordren oppdateres ut fra det fakturerte antallet.  

Når du fakturerer følgesedler på denne måten, eksisterer fortsatt ordrene som følgesedlene ble bokført fra, selv om de er fullstendig levert og fakturert.   

1. Velg ikonet ![Søk etter side eller rapport](media/ui-search/search_small.png "Søk etter side eller rapport"), angi **Slett fakturerte ordrer**, og velg deretter den relaterte koblingen.  
2. Angi hvilke ordrer som skal slettes, i **Nr.** -filterfeltet.  
3. Velg **OK**-knappen.  

Du kan også slette individuelle ordrer manuelt.  

Gjenta trinn 1 til 3 for eventuelle andre berørte dokumenter, for eksempel ordrer.

## <a name="see-also"></a>Se også  
[Salg](sales-manage-sales.md)  
[Arbeide med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

