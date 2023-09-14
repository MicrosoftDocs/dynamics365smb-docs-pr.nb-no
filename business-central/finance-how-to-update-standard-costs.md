---
title: Oppdatere standardkost
description: Du må regelmessig oppdatere standardkostnadene for komponenter og opprullere de nye kostnadene til den overordnede varen.
author: brentholtorf
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.form: 5841
ms.date: 04/01/2021
ms.author: bholtorf
---
# <a name="update-standard-costs"></a>Oppdatere standardkost
Du må regelmessig oppdatere standardkostnadene for komponenter og opprullere de nye kostnadene til den overordnede varen. Prosessen består vanligvis av følgende fire trinn:  

1.  Oppdatere kost på komponent- og kapasitetsnivået. Hvis du vil ha mer informasjon, se kjørselen **Foreslå standardkost for vare**.  
2.  Konsolider og rull opp komponent- og kapasitetskost for å beregne samlet produksjons- eller monteringskost for varene.  
3.  Implementere standardkostnadene som angis når du kjører de forrige kjørslene. Standardkostnadene trer ikke i kraft før de blir implementert. Bruk kjørselen **Implementer standard kostendringer** som oppdaterer endringene i standardkostnad på varene med de i tabellen Standardkost – forslag.  
4.  Implementere endringene for å oppdatere **Enhetskost**-feltet på varekortet og utføre revaluering av lager. Hvis du vil ha mer informasjon, kan du se [Revaluere beholdning](inventory-how-revalue-inventory.md).  

Hvis du vil ha mer informasjon, kan du se [Om beregning av standardkost](finance-about-calculating-standard-cost.md).
  
## <a name="to-update-standard-costs"></a>Slik oppdaterer du standardkost

1.  Kjør kjørselen **Juster kostverdi - vareposter**.  
2.  Kjør kjørselen **Bokfør lagerkost i Finans**.  
3.  Åpne **Standardkost - forslag**, og bruk én eller flere av følgende funksjoner:  

    1.  Kjør kjørselen **Foreslå standardkost for vare**.  
    2.  Gå gjennom resultatene, og foreta nødvendige endringer.  
    3.  Kjør kjørselen **Foreslå standardkost for kapasitet**.  
    4.  Gå gjennom resultatene, og foreta nødvendige endringer.
    5. Kjør kjørselen **Oppruller standardkost**.
    6.  Gå gjennom resultatene, og foreta nødvendige endringer.
    7.  Kjør kjørselen **Implementer endringer i standardkost**.  
4.  Gå gjennom og bokfør siden **Revalueringskladd**, som er fylt ut med poster fra tidligere trinn i denne fremgangsmåten.  

## <a name="see-also"></a>Se også

 [Om beregning av standardkost](finance-about-calculating-standard-cost.md)   
 [Administrere lagerkostnader](finance-manage-inventory-costs.md)   
 [Designdetaljer: Kostmetoder](design-details-costing-methods.md) [Finans](finance.md)  
 [Arbeid med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
