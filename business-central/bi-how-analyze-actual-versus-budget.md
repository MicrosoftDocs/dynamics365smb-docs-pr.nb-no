---
title: Analysere faktiske beløp i forhold til budsjetterte beløp
description: Dette emnet beskriver hvordan du analyserer faktiske beløp kontra budsjetterte beløp som en måte å samle inn, analysere og dele selskapsopplysninger på.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: bi, power BI, analysis, KPI
ms.date: 06/15/2021
ms.author: edupont
ms.openlocfilehash: 2bbdce7c34160ffc1eefc7e398574db8b642b657
ms.sourcegitcommit: 769d20d299155cba30c35636d02b2ef021e4ecc1
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 07/29/2021
ms.locfileid: "6688281"
---
# <a name="analyze-actual-amounts-versus-budgeted-amounts"></a>Analysere faktiske beløp i forhold til budsjetterte beløp
Som en del av innsamling, analyse og deling av selskapsdataene viser du faktiske beløp sammenlignet med budsjetterte beløp for alle konti og for flere perioder.

Hvis du vil analysere budsjetterte beløp, må du først opprette finansbudsjetter. Hvis du vil ha mer informasjon, kan du se [Opprette finansbudsjetter](finance-how-create-budgets.md).

## <a name="to-view-a-gl-budget"></a>Slik viser du et finansbudsjett
I et budsjett med dimensjoner kan du filtrere postene og se de bestemte budsjettene.

1. Velg ikonet ![Lyspære som åpner funksjonen Fortell meg.](media/ui-search/search_small.png "Fortell hva du vil gjøre") , angi **Finansbudsjetter**, og velg deretter den relaterte koblingen.
2. Åpne budsjettet du vil vise, på siden **Finansbudsjetter**.  
3. Øverst på siden fyller du ut feltene etter behov for å definere det som skal vises. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

> [!NOTE]  
>   Hvis du har valgt **Periode** i feltet **Vis som linjer** eller feltet **Vis som kolonner**, må du fylle ut **Vis etter**-feltet. Hvis du ikke har valgt **Periode** i feltet **Vis som linjer** eller feltet **Vis som kolonner**, angir du riktig periode i **Datofilter**-feltet.  

> [!NOTE]  
>   Beregningen tar bare med poster fra finansbudsjettet som har filterkodene du angir på hurtigfanen **Filtre**. Budsjettposter med andre filterkoder, eller uten filterkoder, tas ikke med. Så lenge filteret beholdes på siden, viser budsjettet bare budsjettpostene med disse filterkodene.  

> [!TIP]  
>   Hvis du vil endre budsjettet, kan du endre budsjettpostene. Velg et beløp for å vise de underliggende finansbudsjettpostene.

## <a name="to-view-actual-and-budgeted-amounts-for-all-accounts"></a>Slik viser du faktiske og budsjetterte beløp for alle konti  
Du kan vise finansbudsjetter og sammenligne dem med reelle tall, i flere moduler i [!INCLUDE[prod_short](includes/prod_short.md)].

1. Velg ikonet ![Lyspære som åpner funksjonen Fortell meg.](media/ui-search/search_small.png "Fortell hva du vil gjøre") og angir **Kontoplan** og velger deretter den relaterte koblingen.  
2. På siden **Kontoplan** velger du handlingen **Finanssaldo/Budsjett**.
3. Øverst på siden fyller du ut feltene etter behov for å definere det som skal vises.  
4. Hvis du vil vise en spesifisering som utgjør beløpet som vises, velger du feltet.  

> [!NOTE]  
>   Filtrene du angir på sidetoppteksten, brukes på finansposter og også på budsjettposter.

Kolonnene ytterst til venstre inneholder kontoplanen. Av de fem kolonnene lengst til høyr, viser de fire første de faktiske og budsjetterte debet- og kreditbeløpene for hver konto. Den femte kolonnen viser det proporsjonale forholdet mellom de faktiske og de budsjetterte beløpene på finanskontoen.  

> [!TIP]  
>   Bruk **Vis etter**-feltet på siden **Finanssaldo/budsjett** til å velge periodelengden. Bruk **Vis som**-feltet til å velge hvordan beløpene skal beregnes, **Bevegelse** eller **Saldo per dato**. Velg handlingen **Forrige periode** eller **Neste periode** for å endre perioden.  

## <a name="to-view-actual-and-budgeted-amounts-for-several-periods"></a>Slik viser du faktiske og budsjetterte beløp for flere perioder  
I stedet for å vise de faktiske og budsjetterte beløpene for alle konti i én enkelt periode, kan du vise et antall perioder for én enkelt konto.  

1. Velg ikonet ![Lyspære som åpner funksjonen Fortell meg.](media/ui-search/search_small.png "Fortell hva du vil gjøre") og angir **Kontoplan** og velger deretter den relaterte koblingen.  
2. På siden **Kontoplan** velger du den aktuelle finanskontoen, og deretter velger du handlingen **Finanskontosaldo/Budsjett**.  
3. Øverst på siden fyller du ut feltene etter behov for å definere det som skal vises.   
4. Hvis du vil vise en spesifisering av et beløp som vises, velger du feltet.  

## <a name="see-related-training-at-microsoft-learn"></a>Se relatert opplæring på [Microsoft Learn](/learn/modules/budgets-exchange-rates-dynamics-365-business-central/index)

## <a name="see-also"></a>Se også
[Forretningsintelligens](bi.md)  
[Arbeide med kontoskjemaer](bi-how-work-account-schedule.md)  
[Finans](finance.md)  
[Konfigurere finans](finance-setup-finance.md)  
[Finans og kontoplanen](finance-general-ledger.md)  
[Arbeide med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]