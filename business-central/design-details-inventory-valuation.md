---
title: Designdetaljer – Lagerverdisetting | Microsoft-dokumentasjon
description: Lagerverdisetting er fastsettelse av kostnadene for en lagervare.
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: null
ms.date: 06/08/2021
ms.author: edupont
---
# <a name="design-details-inventory-valuation"></a><a name="design-details-inventory-valuation"></a>Designdetaljer: Lagerverdisetting
Lagerverdisetting fastsettelse av kostnadene som er tilordnet en lagervare, som uttrykt med følgende ligning.  

Sluttbeholdning = startbeholdning + nettokjøp – solgte varers kost  

Beregningen av lagerverdien bruker feltet **Kostbeløp (faktisk)** i verdipostene for varen. Postene klassifiseres i henhold til posttypen som svarer til kostnadskomponentene, direkte kostnad, indirekte kostnad, avvik, revaluering og avrunding. Hvis du vil ha mer informasjon, kan du se [Designdetaljer: Kostkomponenter](design-details-cost-components.md).  

Poster utlignes mot hverandre med ved fast utligning eller i henhold til generell kostflytforutsetning angitt av lagermetoden. Én lagerreduksjonspost kan brukes til flere enn én økningspost med ulike bokføringsdatoer og eventuell annen anskaffelseskost. Hvis du vil ha mer informasjon, kan du se [Designdetaljer: Vareutligning](design-details-item-application.md). Beregningen av lagerverdien for en gitt dato er derfor basert på summering av positive og negative verdiposter.  

## <a name="inventory-valuation-report"></a><a name="inventory-valuation-report"></a>Rapporten Lagerverdisetting
For å beregne lagerverdien i **Lagerverdisetting**-rapporten begynner den ved å beregne verdien til beholdningen for varen på en gitt startdato. Deretter blir verdien av lagerøkningene lagt til, og verdien av lagerreduksjoner opptil en bestemt sluttdato, blir trukket fra. Sluttresultatet er lagerverdien på sluttdatoen. Rapporten beregner disse verdiene ved å summere verdiene i feltet **Kostbeløp (faktisk)** i verdipostene, og bruker bokføringsdatoene som filtre.  

Utskriften av rapporten viser også faktiske beløp, det vil si kostnad for poster som er bokført som fakturerte poster. Rapporten skriver også ut forventet kostnad for poster som er bokført som mottatt eller levert, hvis du velger feltet Ta med forventet kostnad på hurtigfanen Alternativer.  

> [!IMPORTANT]  
>  Verdier i rapporten **Lagerverdisetting** er avstemt med lagerkontoen i finans. Dette betyr at de aktuelle verdipostene er bokført i finans.  

> [!IMPORTANT]  
>  Beløp i **Verdi**-kolonnene i rapporten er basert på bokføringsdatoen for transaksjoner for en vare.  

## <a name="inventory-valuation---wip-report"></a><a name="inventory-valuation---wip-report"></a>Rapporten Lagerverdisetting - VIA
Et produksjonsfirma må fastslå verdien av tre typer beholdning:  

* Råvarerbeholdning  
* VIA-beholdning  
* Ferdige varer på lager  

Verdien til VIA-beholdning fastsettes med formelen nedenfor:  

* Slutt-VIA-beholdning = Start-VIA-beholdning + produksjonskost – kostnader for produserte varer  

Verdipostene er grunnlaget for lagerverdien for kjøpt lagerbeholdning. Beregningen gjøres ved hjelp av verdiene i feltet **Kostbeløp (faktisk)** i verdipostene for vare og kapasitet som er knyttet til en produksjonsordre.  

Formålet med VIA-lagerverdisetting er å fastslå verdien til varer som ennå ikke er ferdigprodusert, på en gitt dato. VIA-lagerverdien er derfor basert på verdipostene som er knyttet til forbruks- og kapasitetspostene. Forbruksposter må faktureres fullstendig på datoen for verdisettingen. Rapporten **Lagerverdisetting – VIA** viser derfor kostnadene som representerer VIA-lagerverdien, i to kategorier: forbruk og kapasitet.  

## <a name="see-also"></a><a name="see-also"></a>Se også
[Designdetaljer: Avstemming med konti i Finans](design-details-reconciliation-with-the-general-ledger.md)   
[Designdetaljer: Revaluering](design-details-revaluation.md)   
[Designdetaljer: Bokføre produksjonsordre](design-details-production-order-posting.md)
[Administrere lagerkostnader](finance-manage-inventory-costs.md)  
[Finans](finance.md)  
[Arbeid med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]
