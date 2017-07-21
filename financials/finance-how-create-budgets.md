---
title: Opprette budsjetter | Microsoft-dokumentasjon
description: "Beskriver hvordan du oppretter budsjetter for å prognostisere ulike økonomiske aktiviteter og tilordne dimensjoner for forretningsanalyseformål."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: postpone
ms.date: 06/16/2017
ms.author: sgroespe
ms.translationtype: Human Translation
ms.sourcegitcommit: 81636fc2e661bd9b07c54da1cd5d0d27e30d01a2
ms.openlocfilehash: 7dfd3cc7efe00b48a39982bb220ccc21b7409da4
ms.contentlocale: nb-no
ms.lasthandoff: 07/07/2017


---
# <a name="how-to-create--budgets"></a>Opprette budsjetter
Du kan ha flere budsjetter for de samme periodene hvis du oppretter budsjetter med forskjellige navn. Først definerer du budsjettnavn og angir budsjettallene. Budsjettnavnet inkluderes da på alle budsjettpostene du oppretter.  

 Når du oppretter et budsjett, kan du definere fire dimensjoner for hvert budsjett. Disse budsjettspesifikke dimensjonene kalles budsjettdimensjoner. Du kan velge budsjettdimensjoner for hvert budsjett, blant de dimensjonene du allerede har definert. Budsjettdimensjoner kan brukes til å definere filtre i budsjetter og til å legge til dimensjonsopplysninger i budsjettposter. Hvis du vil ha mer informasjon, kan du se [Arbeide med dimensjoner](finance-dimensions.md).

 Budsjetter spiller en viktig rolle i forretningsintelligens, for eksempel i årsregnskap basert på kontoskjemaer som inneholder budsjettposter, eller når du analyserer budsjetterte i forhold til faktiske beløp i kontoplanen. Hvis du vil ha mer informasjon, kan du se [Forretningsintelligens](bi.md).   

 > [!NOTE]  
>   Denne funksjonen krever at opplevelsen er satt til **Løsning**. Hvis du vil ha mer informasjon, kan du se [Tilpasse [!INCLUDE[d365fin](includes/d365fin_md.md)]-opplevelsen](ui-experiences.md).  

### <a name="to-create-a-new-budget"></a>Opprette et nytt budsjett  

1. Velg ikonet ![Søk etter side eller rapport](media/ui-search/search_small.png "Ikonet Søk etter side eller rapport"), angi **Finansbudsjetter**, og velg deretter den relaterte koblingen.  
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

