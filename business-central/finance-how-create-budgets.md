---
title: Opprette finansbudsjetter | Microsoft-dokumentasjon
description: Beskriver hvordan du oppretter finansbudsjetter for å prognostisere ulike økonomiske aktiviteter og tilordne dimensjoner for forretningsanalyseformål.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: postpone
ms.date: 01/13/2020
ms.author: sgroespe
ms.openlocfilehash: 5d84dee6ed6cf0b17f488d67e5403638ecb79ce9
ms.sourcegitcommit: ead69ebe5b29927876a4fb23afb6c066f8854591
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 01/14/2020
ms.locfileid: "2953806"
---
# <a name="create-gl-budgets"></a>Opprette finansbudsjetter
Du kan ha flere budsjetter for de samme periodene hvis du oppretter budsjetter med forskjellige navn. Først definerer du budsjettnavn og angir budsjettallene. Budsjettnavnet inkluderes da på alle budsjettpostene du oppretter.  

Når du oppretter et budsjett, kan du definere fire dimensjoner for hvert budsjett. Disse budsjettspesifikke dimensjonene kalles budsjettdimensjoner. Du kan velge budsjettdimensjoner for hvert budsjett, blant de dimensjonene du allerede har definert. Budsjettdimensjoner kan brukes til å definere filtre i budsjetter og til å legge til dimensjonsopplysninger i budsjettposter. Hvis du vil ha mer informasjon, kan du se [Arbeide med dimensjoner](finance-dimensions.md).

Budsjetter spiller en viktig rolle i forretningsintelligens, for eksempel i årsregnskap basert på kontoskjemaer som inneholder budsjettposter, eller når du analyserer budsjetterte i forhold til faktiske beløp i kontoplanen. Hvis du vil ha mer informasjon, kan du se [Forretningsintelligens](bi.md).

I Kostregnskap arbeider du med kostbudsjetter på lignende måte. Hvis du vil ha mer informasjon, kan du se [Opprette kostbudsjetter](finance-create-cost-budgets.md).    

## <a name="to-create-a-new-gl-budget"></a>Opprette et nytt finansbudsjett  
1. Velg ikonet ![Lyspære som åpner Fortell meg-funksjonen](media/ui-search/search_small.png "Fortell hva du vil gjøre"), angi **Finansbudsjetter**, og velg deretter den relaterte koblingen.  
2. Velg handlingen **Rediger oversikt**, og fyll deretter ut feltene etter behov. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]  
3. Velg handlingen **Rediger budsjett**.
4. Øverst på siden **Budsjett** fyller du ut feltene etter behov for å definere det som vises.  

    Bare poster som inneholder budsjettnavnet du har angitt i feltet **Budsjettnavn**, vises. Ettersom budsjettnavnet nettopp er opprettet, finnes det ingen poster som passer til filteret. Siden er derfor tom.  
5. Angi et beløp ved å velge relevant celle i matrisen. **Budsjettposter**-siden åpnes.  
6. Opprett en ny linje, og fyll ut **Beløp**-feltet. Lukk **Budsjettposter**-siden.  
7. Gjenta trinn 5 og 6 til du har angitt alle budsjettbeløpene.  

> [!NOTE]  
>  I hurtigfanen **Filtre** kan du filtrere budsjettopplysningene etter budsjettdimensjoner du har definert under budsjettnavnet.

## <a name="exporting-and-importing-gl-budgets-with-excel"></a>Eksportere og importe finansbudsjetter med Excel
For nesten alle andre sider kan du eksportere data på budsjettsider til Excel for videre behandling eller analyse. Hvis du vil ha mer informasjon, kan du se [Eksportere forretningsdataene til Excel](about-export-data.md).

> [!NOTE]
> Kontoplanen som finansbudsjetter er basert på, har linjer med kontotypen Overskrift som inneholder summen av linjene under. Når du eksporterer et finansbudsjett, eksporteres data på alle linjer uavhengig av kontotypen. Imidlertid kan bare data på linjer av kontotypen Bokføring importeres tilbake. I henhold til dette: <br /><br /> **Når du importerer et finansbudsjett, slettes verdier som finnes i Overskrift-linjene.** <br /><br /> Dette er for å unngå feil totaler når du importerer data som er opprettet eller redigert i Excel.<br /><br /> **Scenario**: Du vet at de nye budsjetterte lønnskostnadene vil bli NOK 1 200 000. Du vil at lønnsavdelingen skal budsjettere for de tre bestemte linjene (av kontotypen Bokføring) for fulltidsansatte, deltidsansatte og midlertidig hjelp. De tre linjene grupperes under en Lønn-overskriftslinje.<br /><br />Du angir 1 200 000 på overskriftslinjen, eksporterer budsjettet til Excel og sender det til lønnsavdelingen og informerer dem om å distribuere NOK 1 200 000.<br /><br /> Lønnsavdelingen fordeler beløpet på tre bokføringskontiene. Når du importerer tilbake til finansbudsjettet, fylles de tre kontiene ut med de nye Excel-dataene, summerer til NOK 1 200 000, og overskriftslinjen er tom.

## <a name="see-related-training-at-microsoft-learnlearnmodulesbudgets-exchange-rates-dynamics-365-business-centralindex"></a>Se relatert opplæring på [Microsoft Learn](/learn/modules/budgets-exchange-rates-dynamics-365-business-central/index)

## <a name="see-also"></a>Se også
[Eksportere forretningsdataene til Excel](about-export-data.md)  
[Finans](finance.md)  
[Forretningsintelligens](bi.md)  
[Konfigurere finans](finance-setup-finance.md)  
[Finans og kontoplanen](finance-general-ledger.md)  
[Arbeide med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)  
