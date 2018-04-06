---
title: Om beregning av standardkost | Microsoft-dokumentasjon
description: "En standard kostprissystem bestemmer lagerenhetskosten basert på noen rimelige historiske eller forventede kostnader. Undersøkelser av tidligere og anslåtte fremtidige kostdata danner grunnlaget for standardkost."
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
ms.sourcegitcommit: bec0619be0a65e3625759e13d2866ac615d7513c
ms.openlocfilehash: 5dc35d82dee8d3a9b93c04de497e7363b7bafb90
ms.contentlocale: nb-no
ms.lasthandoff: 03/22/2018

---
# <a name="about-calculating-standard-cost"></a>Om beregning av standardkost
Mange produksjonsselskaper bruke standardkost som verdisettingsgrunnlag. Dette gjelder også for selskaper som utfører lett produksjon, for eksempel montering og kitting. En standard kostprissystem bestemmer lagerenhetskosten basert på noen rimelige historiske eller forventede kostnader. Undersøkelser av tidligere og anslåtte fremtidige kostdata danner grunnlaget for standardkost. Disse kostnadene fryses til det tas en beslutning om å endre dem. Den faktiske kostnaden for å produsere et produkt kan avvike fra de beregnede standardkostnadene. Når det gjelder administrasjonskontroll, sammenlignes faktisk kostnad med standardkostnad for en bestemt vare, og forskjeller, eller *avvik*, identifiseres og analyseres.  

Standardkost kan vedlikeholdes for varer som etterfylles gjennom kjøp, montering og produksjon. Standardkostnader kan bestå av følgende elementer for hver etterfyllingsmetode.  

|Etterfyllingssystem|Standard kostelementer|  
|--------------------------|----------------------------|  
|**Kjøp**|Direkte materialkostnad og indirekte materialkostnad om nødvendig.|  
|**Montering**|Direkte materialkostnader, direkte eller faste arbeidskostnader og indirekte kostnader.|  
|**Prod.ordre**|Direkte materialkostnader, arbeidskostnader, underleverandørkostnader og indirekte kostnader.|  

## <a name="setting-up-standard-costs"></a>Definere standardkost  
Siden standardkostbeløpet for en produsert eller montert vare kan bestå av flere kostelementer, inkludert materialkost, kapasitetskost (arbeid) og direkte og indirekte underleverandørkost, må standardkost opprettes for hvert av disse elementene.  

Regnskapsoppgaven for et vareproduksjonsselskap som bruker standardkostberegning, er følgende:  

-   Beregne et standardkostbeløp for den ferdige varen og definere det på varekortet.  
-   Registrere og fordele faktisk kost for nøkkelkostelementene, og å gjøre greie for avvik.  

For å fastsette direkte kostnad for en ferdig vare må alle komponentkostbeløpene summeres. En montert eller produsert vare kan inkludere halvfabrikater, som også består av flere komponenter.  

Følgende nøkkelkostelementer utgjør den totale direkte kostnaden for en ferdigbehandlet vare:  

-   Materialkost.  
-   Kapasitetskostnad  
-   Underleverandørkost bare for produserte varer.  

### <a name="material-costs"></a>Materialkost  
 Materialkost er kostnader som er knyttet til delmonteringer og kjøpte råvarer. Materialenhetskost kan bestå av direkte og indirekte kostelementer.  

-   Direkte materialkost representerer et fakturert beløp for kjøpte råmaterialer eller behandlingskost for en halvfabrikat.  
-   Indirekte materialkost, eller *indirekte kostnader*, kan for eksempel representere elementer som lagerføringskost for den ferdige varen etter at den er produsert.  

Defineringen av materialkost for kjøpte varer som påvirker direkte og indirekte kost, avhenger av lagermetoden du har valgt for den angitte varen. Du definerer kostnadsinformasjonen for hver lagemetode på varekortet. Hvis du vil ha mer informasjon, kan du se [Registrere nye varer](inventory-how-register-new-items.md).

Vrakkost (bare for produksjon) er en ytterligere faktor som må tas med i betraktningen når du beregner samlet materialkost. Når en viss mengde råmateriale vrakes under produksjonen eller monteringen av en vare, fører det vanligvis til en økning i antallet komponenter som trengs for å produsere denne varen. Dette øker materialkostbeløpet for komponentene som forbrukes mens en overordnet vare produseres. Du definerer vrakkost for materialer i produksjonsstykklisten eller ruten.  

Materialkostbeløpet for en produsert vare kan representeres på to måter som svarer til følgende grunnlag for standardkostberegning.  

|Basis for kostberegning|Materialkostberegning|  
|----------------------------|-------------------------------|  
|Enkeltnivå|Produsert vare er lik den totale kostnaden for alle kjøpte eller halvfabrikatavarer på den varens produksjonsstykkliste.|  
|Opprullert nivå eller flernivå|Produsert vare er summen av materialkostbeløpet for alle halvfabrikater på stykklisten for varen og kostbeløpet for alle kjøpte varer på produksjonsstykklisten for varen.|  

### <a name="capacity-costs"></a>Kapasitetskost  
Kapasitetskostnader er kostnader som er knyttet til internt arbeid og maskinkostnader. Du må definere disse kostnadene for hver ressurs (i monteringsstyring) og hvert arbeidssenter eller hver produksjonsressurs i ruten (i produksjon). Som med materialer kan du identifisere både direkte og indirekte elementer av kapasitetskost. Direkte kost for et arbeidssenter kan for eksempel være den etablerte produksjonssatsen for å utføre en bestemt funksjon. Indirekte kost for et arbeidssenter kan representere noen generelle fabrikkutgifter, for eksempel belysning, oppvarming og så videre. På lignende måte som med materialkost kan du uttrykke indirekte kapasitetskost som en indirekte kostprosent eller en fast sats for indirekte kost.  

Oppsettet for kapasitetskost for monterte varer består av følgende elementer:  

-   Direkte og indirekte enhetskost for ressursen.  
-   Fast eller direkte ressursbrukstype.  

Oppsettet for kapasitetskost for produserte varer består av følgende elementer:  

-   Direkte og indirekte enhetskost for produksjonsressursen eller arbeidssenteret.  
-   Oppsett av tid og partistørrelse.  

For å beregne standard kapasitetskost må du opprette standardtidssatser som er nødvendige for å utføre operasjoner på produksjonsressurser og arbeidssentre. Samlet tid for å fullføre en operasjon består vanligvis av oppstillings-/operasjonstid samt ventetid og transporttid.  

Du definerer satsene for hver av disse tidstypene for hver produksjonsressurs eller arbeidssenter i en individuell rute.  

> [!NOTE]  
    >  Mens operasjonstidssatser gjelder for hver vareenhet som produseres, gjelder oppstillingstidssatsene for hvert parti. Derfor må du fordele ruteoppstillingstiden for hver operasjon proporsjonalt over partistørrelsen. Du angir partistørrelsen i det tilsvarende feltet i hurtigfanen **Bestilling** på varekortet.  

Hvis du vil angi oppstillingstid i ruten for planlegging, men ikke inkludere denne utgiften i standardkostberegningen, tømmer du feltet **Kost inkl. oppstilling** i vinduet **Produksjonsoppsett**.  

På et enkeltnivågrunnlag er dette arbeidskost som kreves for å produsere den ferdige produksjonsvaren, og angis i ruten for produksjonsvaren. På et flernivågrunnlag er dette kapasitetskost som angitt for hver enkelt produserte vare som er inkludert i stykklisten for den overordnede varen.  

### <a name="subcontractor-costs"></a>Underleverandørkost  
Underleverandørkost er kost som er knyttet til tjenester som leveres av et selskaps eksterne leverandører eller underleverandører. På lignende måte som med material og kapasitet kan underleverandørkost bestå av både direkte og indirekte kostbeløp. Direkte underleverandørkost representerer faktisk avgift for hver serviceenhet som leveres. Indirekte underleverandørkost kan for eksempel representere frakt og håndteringskost som selskapet pådrar seg med en underleveransebestilling.  

Siden underleveranse er en utkontrahert kapasitet, definerer du kostnaden for både direkte og indirekte underleveransetjenester på arbeidssenterkortet som representerer underleveranseoperasjonen.  

## <a name="updating-standard-costs"></a>Oppdatere standardkost  
Hvis du vil oppdatere eller beregne standardkost for monteringsvarer, bruker du funksjonen fra varekortet.  

Prosessen med å oppdatere eller beregne standardkostnader vanligvis består av følgende oppgaver:  

1.  Oppdatere kost på komponent- og kapasitetsnivået. Hvis du vil ha mer informasjon, se kjørslene **Foreslå standardkost for vare** og **Foreslå standardkost for kapasitet**.  
2.  Konsolidere og opprullere komponent- og kapasitetskost for å beregne samlet monterings- eller produksjonskost for varene. Hvis du vil ha mer informasjon, kan du se avsnittet Beregne standardkost for en monteringsvare i [Arbeide med stykklister](inventory-how-work-BOMs.md).  
3.  Implementere standardkostnadene som angis når du kjører de forrige kjørslene. Standardkostnadene trer ikke i kraft før de blir implementert. Hvis du vil ha mer informasjon, se kjørselen **Implementer endringer i standardkost**.  
4.  Implementere endringene for å oppdatere **Enhetskost**-feltet på varekortet og utføre revaluering av lager. Hvis du vil ha mer informasjon, kan du se [Revaluere beholdning](inventory-how-revalue-inventory.md).

## <a name="see-also"></a>Se også  
 [Designdetaljer: Kostmetoder](design-details-costing-methods.md)   
 [Arbeide med stykklister](inventory-how-work-BOMs.md)   
 [Oppdatere standardkost](finance-how-to-update-standard-costs.md)   
 [Designdetaljer: Kostberegning for beholdning](design-details-inventory-costing.md)

