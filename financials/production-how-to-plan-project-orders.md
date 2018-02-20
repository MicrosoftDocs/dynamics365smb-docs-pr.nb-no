---
title: Planlegge prosjektordrer | Microsoft-dokumentasjon
description: "Denne planleggingsoppgaven starter fra en ordre og bruker **Ordreplanlegging**-vinduet. Når du har opprettet en prosjektproduksjonsordre, kan du planlegge den videre ved hjelp av **Ordreplanlegging**-vinduet."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 09/06/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: bec0619be0a65e3625759e13d2866ac615d7513c
ms.openlocfilehash: 27b2571df137b489a72673251fb5a176bfa771fe
ms.contentlocale: nb-no
ms.lasthandoff: 01/30/2018

---
# <a name="plan-project-orders"></a>Planlegge prosjektordrer
Denne planleggingsoppgaven starter fra en ordre og bruker **Ordreplanlegging**-vinduet. Når du har opprettet en prosjektproduksjonsordre, kan du planlegge den videre ved hjelp av **Ordreplanlegging**-vinduet.  

## <a name="to-create-a-project-production-order"></a>Slik oppretter du en prosjektproduksjonsordre  

1.  Velg ikonet ![Søk etter side eller rapport](media/ui-search/search_small.png "Søk etter side eller rapport"), angi **Ordrer**, og velg deretter den relaterte koblingen.  
2.  Velg ordren som representerer produksjonsprosjektet, og velg deretter **Planlegging**-handlingen.  
4.  I **Ordreplanlegging**-vinduet velger du handlingen **Opprett prod.ordre**.  
5.  I vinduet **Opprett ordre fra salg**, i **Ordretype**-feltet velger du **Prosjektordre**.  
6.  Velg **Ja**-knappen.  
7.  Velg ikonet ![Søk etter side eller rapport](media/ui-search/search_small.png "Søk etter side eller rapport"), angi **Produksjonsordrer**, og velg deretter den relaterte koblingen.
8. Åpne produksjonsordren som ble opprettet.  

    Merk at **Kildetype**-feltet i produksjonsordren inneholder **Salgshode**, og ordren har flere linjer, en for hver salgslinjevare som må produseres.  
9. Velg handlingen **Planlegging**.
10. I **Ordreplanlegging**-vinduet velger du handlingen **Forny** for å beregne nytt behov.  

Ordrehodelinjen for prosjektordren vises med alle behovslinjer som ikke er oppfylt, utvidet under hodelinjen. Selv om produksjonsordren inneholder linjer for flere produserte varer, er det totale behovet for alle produksjonsordrelinjer ført opp under én ordrehodelinje i **Ordreplanlegging**-vinduet, og det opprinnelige kundenavnet vises. Du kan deretter fortsette med å planlegge behovet som beskrevet i [Planlegge for nytt behov bestilling for bestilling](production-how-to-plan-for-new-demand.md).  

> [!NOTE]  
>  Behovslinjer i prosjektproduksjonsordren som har **Prod.ordre** i feltet **Etterfyllingssystem**, representerer underliggende produksjonsordrer. Når du har generert disse produksjonsordrene, må du på nytt beregne en plan i vinduet **Ordreplanlegging** for å identifisere eventuelle komponentbehov som ikke er oppfylt. I det tilfellet vises forsyningsordrene som behovslinjer under en vanlig produksjonsordrehodelinje. Dette betyr at prosjektforbindelsen ikke lenger vises i vinduet. Hvis du imidlertid bruker sporingsfunksjonen, kan du lete frem og tilbake i alle forsyningsordrer som er laget under den opprinnelige ordren.  

## <a name="see-also"></a>Se også
[Planlegging](production-planning.md)   
[Definere produksjon](production-configure-production-processes.md)  
[Produksjon](production-manage-manufacturing.md)    
[Lager](inventory-manage-inventory.md)  
[Innkjøp](purchasing-manage-purchasing.md)  
[Designdetaljer: Forsyningsplanlegging](design-details-supply-planning.md)   
[Anbefalte fremgangsmåter for oppsett: Forsyningsplanlegging](setup-best-practices-supply-planning.md)  
[Arbeide med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

