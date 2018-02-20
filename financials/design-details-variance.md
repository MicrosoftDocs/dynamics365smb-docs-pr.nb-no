---
title: "Designdetaljer – Avvik | Microsoft-dokumentasjon"
description: "Avvik er definert som differansen mellom faktisk kost og standardkost, som beskrevet i følgende formel."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 07/01/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 2c13559bb3dc44cdb61697f5135c5b931e34d2a8
ms.openlocfilehash: 04faa28799288e272da93c60cbb90fa19fd190f0
ms.contentlocale: nb-no
ms.lasthandoff: 12/14/2017

---
# <a name="design-details-variance"></a>Designdetaljer: Avvik
Avvik er definert som differansen mellom faktisk kost og standardkost, som beskrevet i følgende formel.  

 faktisk kost – standardkost = avvik  

 Hvis den faktiske kostnaden endres, for eksempel fordi du bokfører et varegebyr på en senere dato, vil avviket bli oppdatert i henhold til dette.  

> [!NOTE]  
>  Revaluering påvirker ikke avviksberegningen, fordi revaluering bare endrer lagerverdien.  

## <a name="example"></a>Eksempel  
 Følgende eksempel illustrerer hvordan avvik beregnes for kjøpte varer. Dette er basert på følgende scenario:  

1.  Brukeren kjøper en vare for NOK 90,00, men standardkosten er NOK 100,00. Derfor blir netto kjøpsavvik NOK -10,00.  
2.  NOK 10,00 krediteres kontoen for kjøpsavvik.  
3.  Brukeren bokfører et varegebyr på NOK 20,00. Den faktiske kostnaden økes derfor til NOK 110,00, og verdien av kjøpsavvik blir NOK 10,00.  
4.  NOK 20,00 debiteres kontoen for kjøpsavvik. Derfor blir netto kjøpsavvik NOK 10,00.  
5.  Brukeren revaluerer varen fra NOK 100,00 til NOK 70,00. Dette påvirker ikke avviksberegningen, bare lagerverdien.  

 Tabellen nedenfor viser de resulterende verdipostene.  

 ![Beregning av kjøpsavvik](media/design_details_inventory_costing_11_purchase_variance.png "design_details_inventory_costing_11_purchase_variance")  

## <a name="determining-the-standard-cost"></a>Fastslå standardkost  
 Standardkosten brukes ved beregning av avvik og beløpet som skal kapitaliseres. Siden standardkosten kan endres over tid på grunn av manuell oppdatering av beregning, trenger du et tidspunkt der standardkost er fast for avviksberegning. Dette er tidspunktet når lagerøkningen faktureres. Punktet der standardkost fastslås når kostnaden justeres for varer som produseres eller monteres.  

 Tabellen nedenfor viser hvordan ulike kostandeler beregnes for produserte og monterte varer når du bruker funksjonen Beregn standardkost.  

|Kostandel|Kjøpt vare|Produsert/montert vare|  
|----------------|--------------------|------------------------------|  
|**Kostpris (standard)**||Materialkostn. - enkeltnivå + Kapasitetskostn. - enkeltnivå + Underlevrd.kostn - enkeltnivå + Indir. kap.kostn - enkeltnivå + Indir. prod.kostn - enkeltnivå|  
|**Materialkostn. - enkeltnivå**|Enhetskost|![Ligning 1](media/design_details_inventory_costing_11_equation_1.png "design_details_inventory_costing_11_equation_1")|  
|**Kapasitetskostn. - enkeltnivå**|Ikke i bruk|![Ligning 2](media/design_details_inventory_costing_11_equation_2.png "design_details_inventory_costing_11_equation_2")|  
|**Underlevrd.kostn - enkeltnivå**|Ikke i bruk|![Ligning 3](media/design_details_inventory_costing_11_equation_3.png "design_details_inventory_costing_11_equation_3")|  
|**Indir. kap.kostn - enkeltnivå**|Ikke i bruk|![Ligning 4](media/design_details_inventory_costing_11_equation_4.png "design_details_inventory_costing_11_equation_4")|  
|**Indir. prod.kostn - enkeltnivå**|Ikke i bruk|(Materialkostn. - enkeltnivå + Kapasitetskostn. - enkeltnivå + Underlevrd.kostn - enkeltnivå) * Indirekte kostnad % / 100 + Sats for indirekte kostnader|  
|**Opprullert materialkost**|Enhetskost|![Ligning 5](media/design_details_inventory_costing_11_equation_5.png "design_details_inventory_costing_11_equation_5")|  
|**Opprullert kapasitetskost**|Ikke i bruk|![Ligning 6](media/design_details_inventory_costing_11_equation_6.png "design_details_inventory_costing_11_equation_6")|  
|**Underlever.kostn. - opprullert**|Ikke i bruk|![Ligning 7](media/design_details_inventory_costing_11_equation_7.png "design_details_inventory_costing_11_equation_7")|  
|**Opprullert indir. kap.kostn.**|Ikke i bruk|![Ligning 8](media/design_details_inventory_costing_11_equation_8.png "design_details_inventory_costing_11_equation_8")|  
|**Opprullert indir. prod.kostn.**|Ikke i bruk|![Ligning 9](media/design_details_inventory_costing_11_equation_9.png "design_details_inventory_costing_11_equation_9")|  

## <a name="see-also"></a>Se også  
 [Designdetaljer: Kostberegning for beholdning](design-details-inventory-costing.md)   
 [Designdetaljer: Kostmetoder](design-details-costing-methods.md) [Administrere lagerkostnader](finance-manage-inventory-costs.md)  
 [Finans](finance.md)  
 [Arbeide med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

