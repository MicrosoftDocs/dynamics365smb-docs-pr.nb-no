---
title: 'Forholdsmessig mva. [NO]'
description: Forbedringer i den norske versjonen gjør det mulig for deg å beregne MVA når både fradragsberettiget og ikke-fradragsberettiget MVA forekommer.
author: brentholtorf
ms.topic: conceptual
ms.devlang: al
ms.search.keywords: null
ms.search.form: '10602, 10697, 10698, 10604'
ms.date: 04/01/2021
ms.author: bholtorf
ms.service: dynamics-365-business-central
---
# <a name="proportional-vat-in-norway"></a>Forholdsmessig mva. i Norge
[!INCLUDE[prod_short](../../includes/prod_short.md)] gjør det mulig for deg å beregne MVA når både fradragsberettiget og ikke-fradragsberettiget MVA forekommer. Siden det er vanskelig å vite hvor og hvordan varen blir brukt, må du ta kontakt med norske skattemyndigheter for å finne ut om en angitt prosentandel MVA kan gå til fradrag basert på historiske data.  

## <a name="example"></a>Eksempel
Et busselskap eier både busser og lastebiler. Når det kjøpes inn bensin, blir denne lagret i én oppbevaringstank. Når bensinen brukes i en buss som transporterer barn, er den ikke fradragsberettiget. Når bensinen brukes i en lastebil, kan den være fradragsberettiget. Avtalen mellom selskapet og de norske skattemyndighetene kan for eksempel da være at 60 % av mva. går til fradrag.  

Hvis du har en kjøpsfaktura på USD 12 500,00 basert på 25 prosent mva., og **Ja** er angitt i **Beregn forholdsmessig fradrag** på siden **Mva-bokføringsoppsett** og feltet **Forholdsmessig fradrags-%** er satt til **60 prosent**, går bare 60 prosent av mva. til fradrag i en kladd. Når fakturaen er bokført, er posteringene som følger:  

- Til leverandøren finanskonto - USD 12 500 (kredit)  
- Til kostkonto 4010 - USD 11 000,00 (debet)  
- Til mva-konto 2720 - USD 1 500,00 (debet)  

Vanligvis ville mva-beløpet bli USD 2 500, basert på 25 prosent mv. Imidlertid går bare 60 prosent til fradrag; mva-beløpet er derfor USD 2 500 x 60 % = USD 1 500. Beløpet på USD 1 000 som ikke er fradragsberettiget, legges til på kostkontoen. Mva-grunnlaget har tilsvarende verdier. Dette beløpet skulle ha vært USD 10 000,00, men siden bare 60 prosent går til fradrag, er grunnlaget USD 6000,00.  

Dette vil også fungere hvis transaksjonen med denne mva-kombinasjonen bokføres via en bestilling.  

> [!NOTE]  
>  Hvis denne funksjonen brukes i en bestilling som brukes til innkjøp av varer til lager, har ikke funksjonen noen innvirkning på varekostnaden. Varekostnaden legges til gjennom ikke-fradragsberettiget mva. Dette er bare tilfelle i forbindelse med finans.  

## <a name="see-also"></a>Se også
 [Beregne forholdsmessig MVA](how-to-calculate-proportional-vat.md)   
 [Norsk mva-rapportering](norwegian-vat-reporting.md)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
