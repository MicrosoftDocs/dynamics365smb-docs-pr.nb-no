---
title: "Eksempelscenario - Definere dynamiske fordelinger basert på solgte varer | Microsoft-dokumentasjon"
description: "Dette emnet viser et eksempel på hvordan du kan definere fordelinger ved hjelp av metoden dynamisk tildeling."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 07/01/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: d7fb34e1c9428a64c71ff47be8bcff174649c00d
ms.openlocfilehash: 3bee6f999a9553bbf8832d3cb65c88080f2d36ef
ms.contentlocale: nb-no
ms.lasthandoff: 03/22/2018

---
# <a name="scenario-example-defining-dynamic-allocations-based-on-items-sold"></a>Eksempelscenario: Definere dynamiske fordelinger basert på solgte varer
Dette emnet viser et eksempel på hvordan du kan definere fordelinger ved hjelp av metoden dynamisk tildeling. I eksemplet endrer du dynamisk fordeling av kostnadene for SALG-kostsenteret slik at det støtter det nye kostobjektet IT-UTSTYR. IT-UTSTYR-pakker har varenumre i området fra 8904-W til 8924-W. Du kan bruke salgstall for fjoråret til å beregne andelen. Tildelingen er bokført til hjelpekosttype 9903.  

> [!NOTE]  
>  I eksempelet brukes demodataene i [!INCLUDE[d365fin](includes/d365fin_md.md)].  

## <a name="to-define-dynamic-allocations-based-on-items-sold-in-the-previous-year"></a>Slik definerer du dynamisk fordelinger basert på varer solgt i fjoråret:  

1.  Velg ikonet ![Søk etter side eller rapport](media/ui-search/search_small.png "Søk etter side eller rapport"), angi **Kostfordelinger**, og velg deretter den relaterte koblingen.  
2.  I vinduet **Kostfordeling** velger du **Ny**.  
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
    >  [!INCLUDE[d365fin](includes/d365fin_md.md)] bruker forrige års salgstall til å beregne en andel av 1596,50 NOK med 100 prosent for IT-UTSTYR-pakker. Dette betyr at alle varene som er solgt det siste året vil bli fordelt til kostobjektet IT-UTSTYR.  

## <a name="see-also"></a>Se også  
 [Angi filtre for dynamisk fordelingsgrunnlag](finance-setting-filters-for-dynamic-allocation-bases.md)   
 [Definere fordelingskilde og -mål](finance-how-to-set-up-allocation-source-and-targets.md)   
 [Definere og fordele kostnader](finance-define-and-allocate-costs.md)   
 [Terminologi i kostregnskap](finance-terminology-in-cost-accounting.md)   
 [Om kostregnskap](finance-about-cost-accounting.md)

