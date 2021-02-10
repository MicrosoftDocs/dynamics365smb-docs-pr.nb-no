---
title: Definere og fordele kostnader | Microsoft-dokumentasjon
description: Kostfordelinger flytter kostnader og inntekter mellom kosttyper, kostsentre og kostobjekter. Du kan definere så mange fordelinger som du trenger.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: 802706f3b501b7c0bdc7959573d5a7c830a7bf90
ms.sourcegitcommit: 2e7307fbe1eb3b34d0ad9356226a19409054a402
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 12/17/2020
ms.locfileid: "4747069"
---
# <a name="defining-and-allocating-costs"></a>Definere og fordele kostnader
Kostfordelinger flytter kostnader og inntekter mellom kosttyper, kostsentre og kostobjekter. Du kan definere så mange fordelinger som du trenger. Hver fordeling består av:  

-   En fordelingskilde.  
-   Ett eller flere tildelingsmål.  

Fordelingskilde fastsetter hvilke kostnader må fordeles, og fordelingsmålene avgjør hvor kostnadene må fordeles. En fordelingskilde kan for eksempel være kostnadene for kostnadstypen Elektrisitet og oppvarming. Du tilordner alle elektrisitets- og oppvarmingskostnader til tre kostsentre: Workshop, Produksjon og Salg. Disse kostsentrene er fordelingsmålene dine.  

For hver fordelingskilde kan du definere du et fordelingsnivå, en gyldighetsperiode og en variant som grupperingsidentifikator. Du kan bruke en kjørsel til å definere filtre for å velge fordelingsdefinisjoner, og deretter kjøre kostfordelinger automatisk.  

For hvert fordelingsmål kan du definere et fordelingsgrunnlag. Fordelingsgrunnlaget kan være statisk eller dynamisk.  

-   Statiske fordelingsgrunnlag er basert på en bestemt verdi, for eksempel kvadratmeter eller et fastsatt fordelingsforhold, for eksempel 5:2:4.  
-   Grunnlaget for dynamisk fordeling avhenger av verdier som kan endres, for eksempel antall ansatte i et kostsenter eller salgsinntekten av et kostobjekt i løpet av en bestemt tidsperiode.  

Tabellen nedenfor beskriver en sekvens av oppgaver, og har koblinger til emnene som beskriver dem.

## <a name="setting-up-allocation-source-and-targets"></a>Definere fordelingskilde og -mål
Hver fordeling består av en fordelingskilde og ett eller flere fordelingsmål. Fordelingskilden fastsetter hvilke kostnader som blir fordelt. Fordelingsmålene fastsetter hvor kostnadene skal fordeles.  

### <a name="to-set-up-cost-allocations"></a>Definere kostfordelinger  
1.  Velg ikonet ![lyspære som åpner Fortell meg-funksjonen](media/ui-search/search_small.png "Fortell hva du vil gjøre"), angi **Kostfordeling**, og velg deretter den relaterte koblingen.  
2.  På siden **Kostfordeling** velger du **Rediger**.  
3.  Angi en ID for fordelingskilde i **ID**-feltet.  
4.  Definer et nivå som et tall mellom 1 og 99 i **Nivå**-feltet. Fordelingsbokføringen vil følge rekkefølgen på nivåene.  
5.  Angi en kosttype for å definere hvilke kosttyper som skal fordeles, i feltet **Kosttypeområde**. Hvis all kost for en kosttype fordeles, defineres ikke område.  
6.  Angi et kostsenter sammen med kostnadene skal fordeles, i feltet **Kostsenterkode**.  
7.  Angi et kostobjekt sammen med kostnadene skal fordeles, i feltet **Kostobjektkode**. Feltet blir som oftest stående tomt, fordi kostobjekter sjelden fordeles på andre kostobjekter.  
8.  Angi en kosttype feltet **Krediter til kosttype**. Fordelt kost krediteres til kildekosttypen. Kreditposten bokføres til kostnadstypen som er gitt her.  
9. På hurtigfanen **Linjer** definerer du tildelingsmålene. På den første linjen angir du en kosttype i feltet **Målkosttype**. Det definerer hvilken kosttype fordelingen debiteres.  
10. På den første linjen angir du første fordelingsmålet i feltet **Målkostsenter** eller **Målkostobjekt**. Disse to feltene definerer hvilket kostsenter eller kostobjekt fordelingen debiteres til. Du kan bare fylle ut ett av disse feltene, og ikke begge.  
11. Gjenta de samme trinnene på den andre linjen for å definere ytterligere fordelingsmål.  
12. Når du har satt opp fordelingsmål og -kilder, velger du **Beregn fordelingsnøkkel** for å beregne totale andelsverdier.  

> [!NOTE]  
>  Merk av for **Blokkert** for å deaktivere tildelingsoppsettet.

## <a name="setting-filters-for-dynamic-allocation-bases"></a>Angi filtre for dynamisk fordelingsgrunnlag
Metoden for dynamisk fordeling er basert på verdier som kan endres. Eksempel: Antall ansatte i et kostsenter eller solgte varer av et kostobjekt i en bestemt tidsperiode. Det finnes ni forhåndsdefinerte fordelingsgrunnlag og tolv dynamiske datointervaller. Du angir ulike filtre basert på fordelingsgrunnlaget.  

### <a name="setting-filters-for-dynamic-allocation-bases"></a>Angi filtre for dynamisk fordelingsgrunnlag  
 Tabellen nedenfor viser hvilke filtre som kan brukes for ulike fordelingsgrunnlag og hvilke verdier som er gyldige i feltene **Nr.filter** og **Gruppefilter**. Trykk på F1 i **Datofilterkode**-feltet for å lese detaljerte beskrivelser.  

|**Base**|**Nr.filter**|**Datofilterkode**|**Kostsenterfilter**|**Kostobjektfilter**|**Gruppefilter**|  
|--------------|----------------------------------------|----------------------------------------------|------------------------------------------------|------------------------------------------------|------------------------------------------|  
|Finansposter|Finanskonto|Ja|Ja|Ja|I/T|  
|Budsjettposter|Finanskonto|Ja|Ja|Ja|Budsjettnavn|  
|Kosttypeposter|Kosttype|Ja|Ja|Ja|I/T|  
|Kostbudsjettposter|Kosttype|Ja|Ja|Ja|Budsjettnavn|  
|Antall ansatte|I/T|Ja|Ja|Ja|I/T|  
|Solgte varer (antall)|Varenr.|Ja|Ja|Ja|Bokføringsgruppe - lager|  
|Kjøpte varer (antall)|Varenr.|Ja|Ja|Ja|Bokføringsgruppe - lager|  
|Solgte varer (beløp)|Varenr.|Ja|Ja|Ja|Bokføringsgruppe - lager|  
|Kjøpte varer (beløp)|Varenr.|Ja|Ja|Ja|Bokføringsgruppe - lager|

## <a name="scenario-1-defining-static-allocations-based-on-allocation-ratio"></a>Scenario 1: Definere statiske fordelinger basert på fordelingsgrad
Statisk fordelingsmetode er basert på en bestemt verdi, for eksempel kvadratmeteren som brukes, eller et fastsatt fordelingsforhold, for eksempel 5:2:4.  

Dette emnet beskriver hvordan du definerer tre nye kostobjekter for fordelingsmål for PROD-kostsenteret for fordelingskilden ved hjelp av det fastsatte fordelingsforholdet på 5:2:4. De tre målkostobjektene er TILBEHØR, MALING og ARMATUR.  

> [!NOTE]  
>  I eksempelet brukes demodataene i [!INCLUDE[prod_short](includes/prod_short.md)].  

### <a name="to-define-the-allocation-source-prod-cost-center-on-the-general-fasttab"></a>Slik definerer du PROD-kostsenteret for fordelingskilden i hurtigfanen Generelt:  

1.  Velg ikonet ![lyspære som åpner Fortell meg-funksjonen](media/ui-search/search_small.png "Fortell hva du vil gjøre"), angi **Kostfordeling**, og velg deretter den relaterte koblingen.  
2.  På siden **Kostfordeling** velger du **Ny**.  
3.  Trykk på Enter eller angi en ID i **ID**-feltet.  
4.  I feltet **Grad** angir du **1**.  
5.  I feltene **Gyldig fra** og **Gyldig til** angir du datoene du vil bruke.  
6.  Angi **PROD** i feltet **Kostsenterkode**-feltet.  
7.  I feltet **Krediter til kosttype** skriver du inn kosttypen **9903**.  

### <a name="to-define-the-allocation-target-cost-objects-on-the-lines-fasttab"></a>Slik definerer du kostobjekter for fordelingsmålene i hurtigfanen Linjer:  

1.  På den første fakturalinjen i feltet **Målkosttype** angir du **9903**.  
2.  På den første fakturalinjen i feltet **Målkostobjekt** angir du **TILBEHØR**.  
3.  På den første linjen, i feltet **Fordelingsmåltype**, velger du **All kost** for å definere hvordan alle påløpte kostnader fordeles.  
4.  På den første linjen i **Grunnlag**-feltet velger du **Statisk** for å bruke den statiske fordelingsmetoden.  
5.  På den første linjen, i feltet **Del**, angir du fordelingsforholdet **5**.  
6.  På den andre fakturalinjen i feltet **Målkosttype** angir du **9903**.  
7.  På den andre fakturalinjen i feltet **Målkostobjekt** angir du **MALING**.  
8.  På den andre linjen, i feltet **Fordelingsmåltype**, velger du **All kost** for å definere hvordan alle påløpte kostnader fordeles.  
9. På den andre linjen i **Grunnlag**-feltet velger du **Statisk** for å bruke den statiske fordelingsmetoden.  
10. På den andre linjen, i feltet **Del**, angir du fordelingsforholdet **2**.  
11. På den tredje fakturalinjen i feltet **Målkosttype** angir du **9903**.  
12. På den tredje fakturalinjen i feltet **Målkostobjekt** angir du **ARMATUR**.  
13. På den tredje linjen, i feltet **Fordelingsmåltype**, velger du **All kost** for å definere hvordan alle påløpte kostnader fordeles.  
14. På den tredje linjen i **Grunnlag**-feltet velger du **Statisk** for å bruke den statiske fordelingsmetoden.  
15. På den tredje linjen, i feltet **Del**, angir du fordelingsforholdet **4**.  

> [!IMPORTANT]  
>  [!INCLUDE[prod_short](includes/prod_short.md)] beregner automatisk **Prosent**-feltet ved å bruke en prosentsats som er avhengige av alle de tre fordelingsforholdene som er angitt i **Del**-feltet for alle de tre linjene.

## <a name="scenario-2-defining-dynamic-allocations-based-on-items-sold"></a>Scenario 2: Definere dynamiske fordelinger basert på solgte varer
Dette emnet viser et eksempel på hvordan du kan definere fordelinger ved hjelp av metoden dynamisk tildeling. I eksemplet endrer du dynamisk fordeling av kostnadene for SALG-kostsenteret slik at det støtter det nye kostobjektet IT-UTSTYR. IT-UTSTYR-pakker har varenumre i området fra 8904-W til 8924-W. Du kan bruke salgstall for fjoråret til å beregne andelen. Tildelingen er bokført til hjelpekosttype 9903.  

> [!NOTE]  
>  I eksempelet brukes demodataene i [!INCLUDE[prod_short](includes/prod_short.md)].  

### <a name="to-define-dynamic-allocations-based-on-items-sold-in-the-previous-year"></a>Slik definerer du dynamisk fordelinger basert på varer solgt i fjoråret:  

1.  Velg ikonet ![lyspære som åpner Fortell meg-funksjonen](media/ui-search/search_small.png "Fortell hva du vil gjøre"), angi **Kostfordelinger**, og velg deretter den relaterte koblingen.  
2.  På siden **Kostfordeling** velger du **Ny**.  
3.  Trykk på Enter eller angi en ID i **ID**-feltet.  
4.  I feltet **Grad** angir du **1**.  
5.  I feltene **Gyldig fra** og **Gyldig til** angir du datoene du vil bruke.  
6.  Angi **SALG** i feltet **Kostsenterkode**-feltet.  
7.  I feltet **Krediter til kosttype** skriver du inn kosttypen **9903**.  
8.  I feltet **Krediter til kosttype** skriver du inn kosttypen **9903**.  
9. Velg **Ny** i feltet **Målkostobjekt** for å opprette det nye kostobjektet IT-UTSTYR, og fyll ut feltene etter behov. Velg **IT-UTSTYR**. La **Målkostsenter**-feltet være tomt.  
10. I feltet **Fordelingsmåltype**, velger du **All kost** for å definere hvordan alle akkumulerte kostnader fordeles.  
11. Velg fordelingsgrunnlaget **Solgte varer (beløp)** i **Grunnlag**-feltet.  
12. I feltet **Nr.filter** skriver du inn **8904-W..8924-W**.  
13. I feltet **Datofilterkode** skriver du inn **I fjor**.  
14. Hvis du vil beregne delen, velger du handlingen **Beregn fordelingsnøkkel**.  

> [!IMPORTANT]  
>  [!INCLUDE[prod_short](includes/prod_short.md)] bruker forrige års salgstall til å beregne en andel av 1596,50 NOK med 100 prosent for IT-UTSTYR-pakker. Dette betyr at alle varene som er solgt det siste året vil bli fordelt til kostobjektet IT-UTSTYR.

## <a name="see-also"></a>Se også  
 [Definere kost.regnskap](finance-set-up-cost-accounting.md)   
 [Overføre og bokføre kostposter](finance-transfer-and-post-cost-entries.md)   
 [Gjøre rede for kostnader](finance-manage-cost-accounting.md)   
 [Terminologi i kostregnskap](finance-terminology-in-cost-accounting.md)   
 [Om kostregnskap](finance-about-cost-accounting.md)
