---
title: Opprette finansbudsjetter | Microsoft-dokumentasjon
description: "Beskriver hvordan du oppretter finansbudsjetter for å prognostisere ulike økonomiske aktiviteter og tilordne dimensjoner for forretningsanalyseformål."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: postpone
ms.date: 10/01/2018
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 9dbd92409ba02281f008246194f3ce0c53e4e001
ms.openlocfilehash: f1311d566a8166a8a8720bb09789f42c65a1b6e7
ms.contentlocale: nb-no
ms.lasthandoff: 09/28/2018

---
# <a name="create-gl-budgets"></a>Opprette finansbudsjetter
Du kan ha flere budsjetter for de samme periodene hvis du oppretter budsjetter med forskjellige navn. Først definerer du budsjettnavn og angir budsjettallene. Budsjettnavnet inkluderes da på alle budsjettpostene du oppretter.  

 Når du oppretter et budsjett, kan du definere fire dimensjoner for hvert budsjett. Disse budsjettspesifikke dimensjonene kalles budsjettdimensjoner. Du kan velge budsjettdimensjoner for hvert budsjett, blant de dimensjonene du allerede har definert. Budsjettdimensjoner kan brukes til å definere filtre i budsjetter og til å legge til dimensjonsopplysninger i budsjettposter. Hvis du vil ha mer informasjon, kan du se [Arbeide med dimensjoner](finance-dimensions.md).

 Budsjetter spiller en viktig rolle i forretningsintelligens, for eksempel i årsregnskap basert på kontoskjemaer som inneholder budsjettposter, eller når du analyserer budsjetterte i forhold til faktiske beløp i kontoplanen. Hvis du vil ha mer informasjon, kan du se [Forretningsintelligens](bi.md).

 Budsjetter spiller en viktig rolle i forretningsintelligens, for eksempel i årsregnskap basert på kontoskjemaer som inneholder budsjettposter, eller når du analyserer budsjetterte i forhold til faktiske beløp i kontoplanen. Hvis du vil ha mer informasjon, kan du se [Forretningsintelligens](bi.md).

I Kostregnskap arbeider du med kostbudsjetter på lignende måte. Hvis du vil ha mer informasjon, kan du se [Opprette kostbudsjetter](finance-create-cost-budgets.md).    

## <a name="to-create-a-new-gl-budget"></a>Opprette et nytt finansbudsjett  
1. Velg ikonet ![lyspære som åpner Fortell meg-funksjonen](media/ui-search/search_small.png "Fortell hva du vil gjøre"), angi **Finansbudsjetter**, og velg deretter den relaterte koblingen.  
2. Velg handlingen **Rediger oversikt**, og fyll deretter ut feltene etter behov. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]  
3. Velg handlingen **Rediger budsjett**.
4. Øverst i vinduet **Budsjett** fyller du ut feltene etter behov for å definere det som vises.  

    Bare poster som inneholder budsjettnavnet du har angitt i feltet **Budsjettnavn**, vises. Ettersom budsjettnavnet nettopp er opprettet, finnes det ingen poster som passer til filteret. Vinduet er derfor tomt.  
5. Angi et beløp ved å velge relevant celle i matrisen. **Budsjettposter**-vinduet åpnes.  
6. Opprett en ny linje, og fyll ut **Beløp**-feltet. Lukk **Budsjettposter**-vinduet.  
7. Gjenta trinn 5 og 6 til du har angitt alle budsjettbeløpene.  

> [!NOTE]  
>  I hurtigfanen **Filtre** kan du filtrere budsjettopplysningene etter budsjettdimensjoner du har definert under budsjettnavnet.   

## <a name="see-also"></a>Se også
[Finans](finance.md)  
[Forretningsintelligens](bi.md)  
[Konfigurere finans](finance-setup-finance.md)  
[Finans og kontoplanen](finance-general-ledger.md)  
[Arbeide med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)  

