---
title: Forholdsmessig MVA
description: Forbedringer i den norske versjonen gjør det mulig for deg å beregne MVA når både fradragsberettiget og ikke-fradragsberettiget MVA forekommer.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/01/2020
ms.author: sgroespe
ms.openlocfilehash: d81d156921a5368e6f7135a12f1de3dd630f4272
ms.sourcegitcommit: 88e4b30eaf6fa32af0c1452ce2f85ff1111c75e2
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 04/01/2020
ms.locfileid: "3181009"
---
# <a name="proportional-vat"></a>Forholdsmessig MVA
[!INCLUDE[d365fin](../../includes/d365fin_md.md)] gjør det mulig for deg å beregne MVA når både fradragsberettiget og ikke-fradragsberettiget MVA forekommer. Siden det er vanskelig å vite hvor og hvordan varen blir brukt, må du ta kontakt med norske skattemyndigheter for å finne ut om en angitt prosentandel MVA kan gå til fradrag basert på historiske data.  

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
