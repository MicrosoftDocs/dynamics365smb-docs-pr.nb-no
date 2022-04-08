---
title: Designdetaljer – Bokføre produksjonsordre | Microsoft-dokumentasjon
description: De forbrukte komponentene og den brukte maskintiden konverteres og avgis som den produserte varen når produksjonsordren er ferdig, på lignende måte som ved bokføring av monteringsordrer.
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 06/08/2021
ms.author: edupont
ms.openlocfilehash: 51d04edb267ba2d75b4ed57d1587b40994f009cc
ms.sourcegitcommit: 8a12074b170a14d98ab7ffdad77d66aed64e5783
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 03/31/2022
ms.locfileid: "8511704"
---
# <a name="design-details-production-order-posting"></a>Designdetaljer: Bokføre produksjonsordre
De forbrukte komponentene og den brukte maskintiden konverteres og avgis som den produserte varen når produksjonsordren er ferdig, på lignende måte som ved bokføring av monteringsordrer. Hvis du vil ha mer informasjon, kan du se [Designdetaljer: Bokføre monteringsordre](design-details-assembly-order-posting.md). Kostnadsflyten for monteringsordrer er imidlertid mindre komplisert, spesielt fordi bokføring av monteringskost bare forekommer én gang og derfor ikke genererer lager for varer i arbeid.


Transaksjoner som skjer under produksjonsprosessen, kan spores gjennom følgende faser:  

1.  Innkjøp av materialer og andre produksjonsmaterialer.  
2.  Konvertere til varer i arbeid.  
3.  Konvertere til ferdige varer på lager.  
4.  Salg av ferdigvarer.  

Derfor må et produksjonsselskap opprette tre separate lagerkonti for å registrere transaksjoner på ulike stadier i produksjonen, i tillegg til vanlige lagerkonti.  

|Lagerkonto|Beskrivelse|  
|-----------------------|---------------------------------------|  
|**Råvarekonto**|Inkluderer kostnader for råvarer som er kjøpt, men som ennå ikke er overført til produksjon. Saldoen på kontoen for råvarer angir kostnaden for disponible råvarer.<br /><br /> Når råvarer flyttes til produksjonsavdelingen, overføres materialkostnadene fra kontoen for råvarer til VIA-kontoen.|  
|**VIA-konto (varer i arbeid)**|Akkumulerer kostnadene som påløper under produksjonen i regnskapsperioden. VIA-kontoen debiteres for kostnaden for råvarer som er overført fra råvarelageret, kostnaden for direkte arbeid som er utført, og indirekte produksjonskostnader som er påløpt.<br /><br /> VIA-kontoen krediteres for den samlede produksjonskosten for enheter som er ferdige på fabrikken og overført til lageret for ferdigvarer.|  
|**Konto for ferdigvarer**|Denne kontoen omfatter samlet produksjonskost for enheter som er ferdige, men ikke solgt ennå. På salgstidspunktet overføres kostnadene for solgte enheter fra kontoen Ferdige varer til kontoen Solgte varers kost.|  

Lagerverdien beregnes ved å spore kostnadene for alle økninger og reduksjoner, slik dette uttrykkes med følgende ligning:  

* lagerverdi = startsaldo for beholdning + verdien av alle økninger - verdien av alle reduksjoner  

Avhengig av beholdningstype representeres økninger og reduksjoner av ulike transaksjoner.  

||Økninger|Nedganger|  
|-|---------------|---------------|  
|**Råvarerbeholdning**|-   Nettokjøp av materiale<br />-   Avgang for halvfabrikater<br />-   Negativt forbruk|Materialforbruk|  
|**VIA-beholdning**|-   Materialforbruk<br />-   Kapasitetsforbruk<br />-   Indir. prod.kostnader|Avgang av sluttvarer (kostnader for produserte varer)|  
|**Ferdige varer på lager**|Avgang av sluttvarer (kostnader for produserte varer)|-   Salg (solgte varers kost)<br />-   Negativ avgang|  
|**Råvarerbeholdning**|-   Nettokjøp av materiale<br />-   Avgang for halvfabrikater<br />-   Negativt forbruk|Materialforbruk|  

Verdiene til økninger og reduksjoner registreres i ulike typer produsert beholdning på samme måte som for kjøpt beholdning. Hver gang det foregår en transaksjon for lagerøkning eller -reduksjon, opprettes det en varepost og en tilsvarende post i Finans for beløpet. Hvis du vil ha mer informasjon, kan du se [Designdetaljer: Lagerbokføring](design-details-inventory-posting.md).  

Selv om transaksjonsverdiene som er knyttet til kjøpte varer bare posteres som vareposter med tilknyttede verdiposter, blir transaksjoner som er knyttet til produserte varer bokført som kapasitetsposter med tilknyttede verdiposter, i tillegg til varepostene.  

## <a name="posting-structure"></a>Bokføringsstruktur  
Bokføring av produksjonsordrer i VIA-beholdningen omfatter avgang, forbruk og kapasitet.  

Diagrammet nedenfor viser de involverte bokføringsrutinene i kodeenhet 22.  

![Bokføringsrutiner for produksjonsordrer.](media/design_details_inventory_costing_14_production_posting_1.png "Bokføringsrutiner for produksjonsordrer")  

Diagrammet nedenfor viser tilknytningene mellom de resulterende postene og kostobjektene.  

![Produksjonspostflyt.](media/design_details_inventory_costing_14_production_posting_2.png "Produksjonspostflyt")  

Kapasitetsposten beskriver kapasitetsforbruket i tidsenheter, mens den tilknyttede verdiposten beskriver verdien til det bestemte kapasitetsforbruket.  

Vareposten beskriver materialforbruket eller avgangen uttrykt i antall, mens den tilknyttede verdiposten beskriver verdien til dette bestemte materialforbruket eller denne bestemte avgangen.  

En verdipost som beskriver VIA-beholdningsverdi kan knyttes til én av følgende kombinasjoner av kostobjekter:  

-   En produksjonsordrelinje, en arbeids- eller produksjonsressurs og en kapasitetspost.  
-   En produksjonsordrelinje, en vare og en varepost.  
-   Bare en produksjonsordre  

Hvis du vil ha mer informasjon om hvordan kostnader fra produksjon og montering bokføres i Finans, kan du se [Designdetaljer: Lagerbokføring](design-details-inventory-posting.md).  

## <a name="capacity-posting"></a>Kapasitetsbokføring  
Bokføring av avgang fra siste produksjonsordrerutelinjen fører til en kapasitetspost for sluttvaren, i tillegg til en lagerøkning.  

 Kapasitetsposten er en registrering av tiden som er brukt på å produsere varen. Den tilknyttede verdiposten beskriver økningen i VIA-beholdningsverdien, som er verdien til konverteringskostnaden. Hvis du vil ha mer informasjon, kan du se "Fra Kapasitetspost" i [Designdetaljer: Konti i Finans](design-details-accounts-in-the-general-ledger.md).  

## <a name="production-order-costing"></a>Produksjonsordrekostnad  
 For å kunne styre lager- og produksjonskostnader må et produksjonsselskap måle kostnaden for produksjonsordrer, fordi den forhåndsdefinerte standardkosten for hver produserte vare kapitaliseres i balansen. Hvis du vil ha informasjon om hvorfor produserte varer bruker lagermetoden Standard, kan du se [Designdetaljer: Kostmetoder](design-details-costing-methods.md).  

> [!NOTE]  
>  I miljøer som ikke bruker lagermetoden Standard, blir faktisk kost kapitalisert i balansen i stedet for standardkost for produserte varer.  

Den faktiske kostnaden for en produksjonsordre består av følgende kostnadskomponenter:  

-   Faktisk materialkostnad  
-   Faktisk kapasitetskost eller underleverandørkost  
-   Indirekte produksjonskostnader  

Disse faktiske kostnadene bokføres i produksjonsordren og sammenlignes med standardkostnadene for å beregne avvik. Avvik beregnes for hver av varekostkomponentene: råvarer, kapasitet, underleverandør, indirekte kapasitet og produksjonskostnader. Avvikene kan analyseres for å fastslå problemer, for eksempel for mye svinn i behandling.  

I standardkostmiljøer er kostberegning for en produksjonsordre basert på følgende mekanisme:  

1.  Når den siste ruteoperasjonen bokføres, bokføres produksjonsordrekostnaden i vareposten og settes til forventet kostnad.  

    Denne kostnaden er lik avgangsantallet som bokføres i ferdigmeldingskladden, ganget med standardkosten som kopieres fra varekortet. Kostnaden behandles som forventet kost til produksjonsordren er fullført. Hvis du vil ha mer informasjon, kan du se [Designdetaljer: Bokføre forventet kost](design-details-expected-cost-posting.md).  

    > [!NOTE]  
    >  Dette er forskjellig fra bokføring av monteringsordrer, der det alltid er faktiske kostnader som bokføres. Hvis du vil ha mer informasjon, kan du se [Designdetaljer: Bokføre monteringsordre](design-details-assembly-order-posting.md).  
2.  Når **Ferdig** angis for produksjonsordren, faktureres ordren ved å kjøre kjørselen **Juster kostverdi - vareposter**. Resultatet blir at de totale kostnadene for ordren beregnes basert på standardkost for brukte materialer og kapasitet. Avvikene mellom de beregnede standardkostnadene og de faktiske produksjonskostnadene beregnes og bokføres.  

## <a name="see-also"></a>Se også  
 [Designdetaljer: Kostberegning for beholdning](design-details-inventory-costing.md)   
 [Designdetaljer: Bokføre monteringsordre](design-details-assembly-order-posting.md)  
 [Administrere lagerkostnader](finance-manage-inventory-costs.md) [Finans](finance.md)  
 [Arbeid med Business Central](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]