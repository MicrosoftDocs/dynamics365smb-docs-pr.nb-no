---
title: Planlegge prosjektordrer | Microsoft-dokumentasjon
description: "Denne planleggingsoppgaven starter fra en ordre og bruker **Ordreplanlegging**-siden. Når du har opprettet en prosjektproduksjonsordre, kan du planlegge den videre ved hjelp av **Ordreplanlegging**-siden."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 10/01/2018
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 33b900f1ac9e295921e7f3d6ea72cc93939d8a1b
ms.openlocfilehash: 4cb63a7dc26e13c7947ba2ae071c3dff87c53e9d
ms.contentlocale: nb-no
ms.lasthandoff: 11/26/2018

---
# <a name="plan-project-orders"></a>Planlegge prosjektordrer
Denne planleggingsoppgaven starter fra en ordre og bruker **Ordreplanlegging**-siden. Når du har opprettet en prosjektproduksjonsordre, kan du planlegge den videre ved hjelp av **Ordreplanlegging**-siden.  

## <a name="to-create-a-project-production-order"></a>Slik oppretter du en prosjektproduksjonsordre  

1.  Velg ikonet ![lyspære som åpner Fortell meg-funksjonen](media/ui-search/search_small.png "Fortell hva du vil gjøre") ikonet, angi **Ordrer**, og velg deretter den relaterte koblingen.  
2.  Velg ordren som representerer produksjonsprosjektet, og velg deretter **Planlegging**-handlingen.  
4.  På **Ordreplanlegging**-siden velger du handlingen **Opprett prod.ordre**.  
5.  På siden **Opprett ordre fra salg** velger du **Prosjektordre** i **Ordretype**-feltet.  
6.  Velg **Ja**-knappen.  
7.  Velg ikonet ![lyspære som åpner Fortell meg-funksjonen](media/ui-search/search_small.png "Fortell hva du vil gjøre"), angi **Produksjonsordrer**, og velg deretter den relaterte koblingen.
8. Åpne produksjonsordren som ble opprettet.  

    Merk at **Kildetype**-feltet i produksjonsordren inneholder **Salgshode**, og ordren har flere linjer, en for hver salgslinjevare som må produseres.  
9. Velg handlingen **Planlegging**.
10. På siden **Ordreplanlegging** velger du handlingen **Forny** for å beregne nytt behov.  

Ordrehodelinjen for prosjektordren vises med alle behovslinjer som ikke er oppfylt, utvidet under hodelinjen. Selv om produksjonsordren inneholder linjer for flere produserte varer, er det totale behovet for alle produksjonsordrelinjer ført opp under én ordrehodelinje på **Ordreplanlegging**-siden, og det opprinnelige kundenavnet vises. Du kan deretter fortsette med å planlegge behovet som beskrevet i [Planlegge for nytt behov bestilling for bestilling](production-how-to-plan-for-new-demand.md).  

> [!NOTE]  
>  Behovslinjer i prosjektproduksjonsordren som har **Prod.ordre** i feltet **Etterfyllingssystem**, representerer underliggende produksjonsordrer. Når du har generert disse produksjonsordrene, må du på nytt beregne en plan på siden **Ordreplanlegging** for å identifisere eventuelle komponentbehov som ikke er oppfylt. I det tilfellet vises forsyningsordrene som behovslinjer under en vanlig produksjonsordrehodelinje. Dette betyr at prosjektforbindelsen ikke lenger vises på siden. Hvis du imidlertid bruker sporingsfunksjonen, kan du lete frem og tilbake i alle forsyningsordrer som er laget under den opprinnelige ordren.  

## <a name="see-also"></a>Se også
[Planlegging](production-planning.md)   
[Definere produksjon](production-configure-production-processes.md)  
[Produksjon](production-manage-manufacturing.md)    
[Lager](inventory-manage-inventory.md)  
[Innkjøp](purchasing-manage-purchasing.md)  
[Designdetaljer: Forsyningsplanlegging](design-details-supply-planning.md)   
[Anbefalte fremgangsmåter for oppsett: Forsyningsplanlegging](setup-best-practices-supply-planning.md)  
[Arbeide med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

