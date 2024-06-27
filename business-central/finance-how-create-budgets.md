---
title: Opprett finansbudsjetter
description: Beskriver hvordan du oppretter finansbudsjetter for å prognostisere ulike økonomiske aktiviteter og tilordne dimensjoner for forretningsanalyseformål.
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bholtorf
ms.topic: conceptual
ms.devlang: al
ms.search.keywords: postpone
ms.search.form: '113, 120, 121, 154, 350, 422, 7132, 7133, 7138, 7139, 9203, 9219, 9239, 9373, 9374'
ms.date: 06/10/2024
ms.service: dynamics-365-business-central
---
# Opprett finansbudsjetter

Du kan ha flere budsjetter for de samme periodene hvis du oppretter budsjetter med forskjellige navn. Først definerer du budsjettnavn og angir budsjettallene. Budsjettnavnet inkluderes da på alle budsjettpostene du oppretter.  

Når du oppretter et budsjett, kan du tilordne budsjettspesifikke dimensjoner, kalt budsjettdimensjoner, for det. Du kan bruke budsjettdimensjoner til å definere filtre i budsjetter og til å legge til dimensjonsopplysninger i budsjettposter. Finn ut mer under [Arbeide med dimensjoner](finance-dimensions.md).

Budsjetter spiller en viktig rolle i Business Intelligence. Eksempler inneholder et regnskap basert på finansrapporter som inneholder budsjettposter, eller når du analyserer budsjetterte i forhold til faktiske beløp i kontoplanen. Finn ut mer om [Forretningsintelligens](bi.md).

I Kostregnskap arbeider du med kostbudsjetter på lignende måte. Lære mer om [Opprette kostbudsjetter](finance-create-cost-budgets.md).  

## Opprette et nytt finansbudsjett

1. Velg ikonet ![Lyspære som åpner funksjonen Fortell meg.](media/ui-search/search_small.png "Fortell hva du vil gjøre") , angi **Finansbudsjetter**, og velg deretter den relaterte koblingen.  
2. Velg handlingen **Rediger oversikt**, og fyll deretter ut feltene etter behov. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]  
3. Velg handlingen **Rediger budsjett**.
4. Øverst på siden **Budsjett** fyller du ut feltene etter behov for å definere det som vises.  

   Siden viser bare poster som inneholder budsjettnavnet du har angitt i feltet **Budsjettnavn**. Fordi du akkurat har opprettet budsjettnavnet, finnes det ingen poster som passer til filteret. Siden er derfor tom.  
5. Angi et beløp ved å velge relevant celle i matrisen. **Budsjettposter**-siden åpnes.  
6. Opprett en ny linje, og fyll ut **Beløp**-feltet. Lukk **Budsjettposter**-siden.  
7. Gjenta trinn 5 og 6 for alle beløp i budsjettet.  

> [!NOTE]  
> I hurtigfanen **Filtre** kan du filtrere budsjettopplysningene etter budsjettdimensjoner du har definert under budsjettnavnet.

## Eksportere og importere finansbudsjetter med Excel

For nesten alle andre sider kan du eksportere data på budsjettsider til Microsoft Excel for videre behandling eller analyse. Lær mer på [Eksportere forretningsdataene til Excel](about-export-data.md).

> [!NOTE]
> Kontoplanen, som finansbudsjetter er basert på, har linjer med kontotypen Overskrift. Disse linjene inneholder summen av linjene under. Når du eksporterer et finansbudsjett, eksporterer du data på alle linjer uavhengig av kontotypen. Du kan imidlertid bare importere data på linjer av kontotypen Bokføring.

Når du importerer et finansbudsjett, slettes verdier som finnes i Overskrift-linjene. De slettes for å unngå feil totalsummer etter at du har importert data som ble opprettet eller redigert i Excel.

### Scenario

Du vet at de nye budsjetterte lønnskostnadene vil bli lokal valuta (LCY) 1 200 000. Du vil at lønnsavdelingen skal budsjettere for de tre bestemte linjene (av kontotypen Bokføring) for fulltidsansatte, deltidsansatte og midlertidig hjelp. De tre linjene grupperes under en Lønn-overskriftslinje.

Du angir 1 200 000 på overskriftslinjen, eksporterer budsjettet til Excel og sender det til lønnsavdelingen og informerer dem om å distribuere LV 1 200 000.

Lønnsavdelingen fordeler beløpet på tre bokføringskontiene. Når du importerer tilbake til finansbudsjettet, fylles de tre kontiene ut med de nye Excel-dataene, summerer til LV 1 200 000, og overskriftslinjen er tom.

## Se også

[Eksporter forretningsdataene til Excel](about-export-data.md)  
[Finans](finance.md)  
[Forretningsintelligens](bi.md)  
[Konfigurere finans](finance-setup-finance.md)  
[Finans og kontoplanen](finance-general-ledger.md)  
[Arbeid med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
