---
title: Beregne etterfylling av hylle | Microsoft-dokumentasjon
description: Når lokasjonen er definert til å bruke lagerstyring, tas det hensyn til prioriteringene av plasseringsmalene for lokasjonen ved plassering av mottak.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: 4135547ae45f561a84b7952ecec07f8d4abad437
ms.sourcegitcommit: 2e7307fbe1eb3b34d0ad9356226a19409054a402
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 12/17/2020
ms.locfileid: "4759920"
---
# <a name="calculate-bin-replenishment"></a>Beregn etterfylling av hylle
Når lokasjonen er definert til å bruke lagerstyring, tas det hensyn til prioriteringene av plasseringsmalene for lokasjonen ved plassering av mottak. Prioriteter inkluderer minimums- og maksimumsantall for hylleinnhold som er fastsatt for en bestemt hylle, og hylleprioriteringene. Hvis varene ankommer jevnlig, vil de mest brukte plukkhyllene derfor bli fylt opp etter hvert som de blir tømt.  

Lagerbeholdningen ankommer imidlertid ikke alltid jevnt. Noen ganger kjøpes varer i store antall slik at selskapet kan få en rabatt, eller produksjonsenheten kan produsere en stor mengde av én vare for å oppnå en lav enhetskostnad. Varene vil deretter ikke bli mottatt i lageret igjen på en stund, og lageret må jevnlig flytte varer til plukkhyller fra masselagringsområder.  

Det kan også være at lageret forventer at en lagervare skal ankomme snart, og ønsker å tømme masselagringsområdet for varer før de nye varene ankommer.  

Og endelig, hvis du har definert masselagringshyllene med bare hylletypehandlingen **Plassering**, som betyr at **Plukk**-handlingen ikke er valg for hylletypen, må du alltid sørge for etterfylling av plukkhyllene, fordi en plukking av beholdning ikke foreslås for hyller av typen Plassering.  

## <a name="to-replenish-pick-bins"></a>Slik etterfyller du plukkhyller  
1.  Velg ikonet ![Lyspære som åpner Fortell meg-funksjonen](media/ui-search/search_small.png "Fortell hva du vil gjøre"), angi **Flytteforslag**, og velg deretter den relaterte koblingen.  
2.  Velg handlingen **Beregn etterfylling av hylle** for åpne rapportforespørselssiden.  
3.  Fyll ut kjørselssiden for å begrense omfanget av etterfyllingsforslaget som skal beregnes. Du kan for eksempel ønske å begrense deg til bestemte varer, soner eller hyller.  
4.  Velg **OK**-knappen. Det opprettes linjer for etterfyllingsflyttingene som må utføres, i henhold til reglene som er definert for hyllene og hylleinnholdet, det vil si varer i hyller.  
5.  Hvis du ønsker å utføre alle de foreslåtte etterfyllingene, velger du **Opprett flytting**-handlingen. De ansatte kan nå finne instruksjoner på menyelementet **Flyttinger**, utføre dem og registrere dem.  
6.  Hvis du bare vil at noen av forslagene skal utføres, sletter du de linjene som er mindre viktige, og deretter oppretter du en flytting.  

Neste gang du beregner etterfylling av en hylle, vil forslagene du har slettet, bli opprettet på nytt hvis de fremdeles er gyldige på det tidspunktet.  

> [!NOTE]  
>  Hvis følgende betingelser er oppfylt for en vare:  
>   
>  -   varen har en utløpsdato  
> -   Feltet **Plukk i henhold til FEFO** er merket av på lokasjonskortet, og  
> -   Du bruker funksjonaliteten **Beregn etterfylling av hyller**  
>   
>  vil feltene **Fra sone** og **Fra hylle** være tomme fordi algoritmen for å beregne hvor varene skal flyttes fra, bare utløses når du aktiverer funksjonen **Opprett flytting**.  

## <a name="see-also"></a>Se også  
[Lagerstyring](warehouse-manage-warehouse.md)  
[Plukking etter FEFO](warehouse-picking-by-fefo.md)  
[Lager](inventory-manage-inventory.md)  
[Definere lagerstyring](warehouse-setup-warehouse.md)     
[Monteringsstyring](assembly-assemble-items.md)    
[Designdetaljer: Lagerstyring](design-details-warehouse-management.md)  
[Arbeide med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)
