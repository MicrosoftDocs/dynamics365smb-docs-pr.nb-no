---
title: Designdetaljer – Konti i Finans | Microsoft-dokumentasjon
description: Hvis du vil avstemme lager- og kapasitetsposter med Finans, bokføres de tilknyttede verdipostene på ulike konti i finans.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: c5129a8b8116eab9996a47ad82b2579658a45b8b
ms.sourcegitcommit: 2e7307fbe1eb3b34d0ad9356226a19409054a402
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 12/17/2020
ms.locfileid: "4751883"
---
# <a name="design-details-accounts-in-the-general-ledger"></a>Designdetaljer: Konti i Finans
Hvis du vil avstemme lager- og kapasitetsposter med Finans, bokføres de tilknyttede verdipostene på ulike konti i finans. Hvis du vil ha mer informasjon, se [Designdetaljer: Avstemming med konti i Finans](design-details-reconciliation-with-the-general-ledger.md).  

## <a name="from-the-inventory-ledger"></a>Fra varepost  
Følgende tabell viser relasjonen mellom ulike typer verdiposter for beholdning og kontiene og motkontiene i finans.  

|**Vareposttype**|**Verdiposttype**|**Avvikstype**|**Forventet kostnad**|**Konto**|**Motkonto**|  
|--------------------------------|--------------------------|-----------------------|-----------------------|-----------------|---------------------------|  
|Kjøp|Kjøpspris/prod.kost||Ja|Lager (midlertidig)|Forv. lagerjust.kto. (midl.)|  
|Kjøp|Kjøpspris/prod.kost||Nei|Lager|Utlignet kjøpspris/prod.kost|  
|Kjøp|Indirekte kost||Nei|Lager|Utlignet indirekte kostnad|  
|Kjøp|Avvik|Kjøp|Nei|Lager|Kjøpsavvik|  
|Kjøp|Revaluering||Nei|Lager|Lagerjustering|  
|Kjøp|Avrunding||Nei|Lager|Lagerjustering|  
|Salg|Kjøpspris/prod.kost||Ja|Lager (midlertidig)|Vareforbruk (midlertidig)|  
|Salg|Kjøpspris/prod.kost||Nei|Lager|VAREFORBR|  
|Salg|Revaluering||Nei|Lager|Lagerjustering|  
|Salg|Avrunding||Nei|Lager|Lagerjustering|  
|Oppjustering,Nedjustering,Overføring|Kjøpspris/prod.kost||Nei|Lager|Lagerjustering|  
|Oppjustering,Nedjustering,Overføring|Revaluering||Nei|Lager|Lagerjustering|  
|Oppjustering,Nedjustering,Overføring|Avrunding||Nei|Lager|Lagerjustering|  
|(Produksjon) Forbruk|Kjøpspris/prod.kost||Nei|Lager|VIA|  
|(Produksjon) Forbruk|Revaluering||Nei|Lager|Lagerjustering|  
|(Produksjon) Forbruk|Avrunding||Nei|Lager|Lagerjustering|  
|Monteringsforbruk|Kjøpspris/prod.kost||Nei|Lager|Lagerjustering|  
|Monteringsforbruk|Kjøpspris/prod.kost||Nei|Utlignet kjøpspris/prod.kost|Lagerjustering|  
|Monteringsforbruk|Indirekte kost||Nei|Utlignet indirekte kostnad|Lagerjustering|  
|(Produksjon) Avgang|Kjøpspris/prod.kost||Ja|Lager (midlertidig)|VIA|  
|(Produksjon) Avgang|Kjøpspris/prod.kost||Nei|Lager|VIA|  
|(Produksjon) Avgang|Indirekte kost||Nei|Lager|Utlignet indirekte kostnad|  
|(Produksjon) Avgang|Avvik|Materiale|Nei|Lager|Materialavvik|  
|(Produksjon) Avgang|Avvik|Kapasitet|Nei|Lager|Kapasitetsavvik|  
|(Produksjon) Avgang|Avvik|Underleveranse|Nei|Lager|Avvik i underleveranse|  
|(Produksjon) Avgang|Avvik|Indir. kap.kostn.|Nei|Lager|Avvik i indir. kap.kostn.|  
|(Produksjon) Avgang|Avvik|Indir. prod.kostnader|Nei|Lager|Avvik i indir. prod.kostn.|  
|(Produksjon) Avgang|Revaluering||Nei|Lager|Lagerjustering|  
|(Produksjon) Avgang|Avrunding||Nei|Lager|Lagerjustering|  
|Monteringsavgang|Kjøpspris/prod.kost||Nei|Lager|Lagerjustering|  
|Monteringsavgang|Revaluering||Nei|Lager|Lagerjustering|  
|Monteringsavgang|Indirekte kost||Nei|Lager|Utlignet indirekte kostnad|  
|Monteringsavgang|Avvik|Materiale|Nei|Lager|Materialavvik|  
|Monteringsavgang|Avvik|Kapasitet|Nei|Lager|Kapasitetsavvik|  
|Monteringsavgang|Avvik|Indir. kap.kostn.|Nei|Lager|Avvik i indir. kap.kostn.|  
|Monteringsavgang|Avvik|Indir. prod.kostnader|Nei|Lager|Avvik i indir. prod.kostn.|  
|Monteringsavgang|Avrunding||Nei|Lager|Lagerjustering|  

## <a name="from-the-capacity-ledger"></a>Fra kapasitetsposten  
 Følgende tabell viser relasjonen mellom ulike typer verdiposter for kapasitet og kontiene og motkontiene i finans. Kapasitetsposter representerer arbeidtidsforbruket under monterings- eller produksjonsarbeid.  

|**Arbeidstype**|**Kapasitetsposttype**|**Verdiposttype**|**Konto**|**Motkonto**|  
|-------------------|------------------------------------|--------------------------|-----------------|---------------------------|  
|Montering|Ressurs|Kjøpspris/prod.kost|Utlignet kjøpspris/prod.kost|Lagerjustering|  
|Montering|Ressurs|Indirekte kost|Utlignet indirekte kostnad|Lagerjustering|  
|Produksjon|Produksjonsressurs/Arbeidssenter|Kjøpspris/prod.kost|VIA-konto|Utlignet kjøpspris/prod.kost|  
|Produksjon|Produksjonsressurs/Arbeidssenter|Indirekte kost|VIA-konto|Utlignet indirekte kostnad|  

## <a name="assembly-costs-are-always-actual"></a>Monteringskostnader er alltid faktiske  
 Monteringsbokføringer vises ikke i midlertidige konti, som vist i tabellen ovenfor. Dette er fordi begrepet om varer i arbeid (VIA) ikke gjelder i bokføring av monteringsavgang, i motsetning til i bokføring av produksjonsavgang. Monteringskostnader bokføres bare som faktiske kostnader, aldri som forventede kostnader.  

 Hvis du vil ha mer informasjon, kan du se [Designdetaljer: Bokføre monteringsordre](design-details-assembly-order-posting.md).  

## <a name="calculating-the-amount-to-post-to-the-general-ledger"></a>Beregne beløpet som skal bokføres i Finans  
 Følgende felt i **Verdipost**-tabellen brukes til å beregne det forventede kostnadsbeløpet som bokføres i finans:  

-   Kostbeløp (faktisk)  
-   Bokført kost  
-   Kostbeløp (forventet)  
-   Forventet kost bokført i Finans  

Tabellen nedenfor viser hvordan beløpene som skal bokføres i finans, beregnes for de to ulike kosttypene.  

|Kosttp.|Beregning|  
|---------------|-----------------|  
|Faktisk kostnad|Kostbeløp (faktisk) – kost bokført til finans|  
|Forventet kostnad|Kostbeløp (forventet) – Forventet kost bokført i Finans|  

## <a name="see-also"></a>Se også  
 [Designdetaljer: Kostberegning for beholdning](design-details-inventory-costing.md)   
 [Designdetaljer: Lagerbokføring](design-details-inventory-posting.md)   
 [Designdetaljer: Bokføre forventet kost](design-details-expected-cost-posting.md)  
 [Administrere lagerkostnader](finance-manage-inventory-costs.md)  
 [Finans](finance.md)  
 [Arbeide med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]