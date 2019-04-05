---
title: Definere ressurskostpriser, priser og kapasitet | Microsoft-dokumentasjon
description: For å bruke ressurser og forenkle prosjektstyring angir du kostnadene og prisene for individuelle ressurser eller ressursgrupper, og angir ressurskapasiteten.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: project management, capacity, staff
ms.date: 10/01/2018
ms.author: sgroespe
ms.openlocfilehash: 362f335fa313dce9a4e75c962ef6f5a2f01ec5fd
ms.sourcegitcommit: 1bcfaa99ea302e6b84b8361ca02730b135557fc1
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 03/08/2019
ms.locfileid: "803213"
---
# <a name="set-up-resources"></a>Definere ressurser
For å behandle ressursaktiviteter på riktig måte må du definere ressursene og de relaterte kostnadene og prisene. De prosjektrelaterte prisene, rabattene og kostfaktorreglene er definert på prosjektkortet. Du kan angi kostnadene og prisene for individuelle ressurser, ressursgrupper eller alle tilgjengelige ressurser for firmaet.

Når ressurser brukes eller selges i et prosjekt, hentes de tilknyttede prisene og kostnadene fra informasjonen du definerer.

Du angir standardbeløpet per time når ressursen opprettes. Hvis du for eksempel bruker en bestemt maskin i fem timer på et prosjekt, beregnes prosjektet basert på beløpet per time.

## <a name="to-set-up-a-resource"></a>Slik konfigurerer du en ressurs
Opprette et kort for hver ressurs du vil bruke i prosjekter.

1. Velg ikonet ![lyspære som åpner Fortell meg-funksjonen](media/ui-search/search_small.png "Fortell hva du vil gjøre"), angi **Ressurser**, og velg deretter den relaterte koblingen.
2. Velg handlingen **Ny**.
3. Fyll ut feltene etter behov. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]  

## <a name="to-set-up-a-resource-group"></a>Slik definerer du en ressursgruppe
Du kan kombinere flere ressurser i én ressursgruppe. Alle kapasiteter og budsjetter for ressursgrupper akkumuleres fra de enkelte ressursene. Det er også mulig å angi kapasiteter for ressursgrupper, enten uavhengig av akkumulerte verdier eller i tillegg til disse.

1. Velg ikonet ![lyspære som åpner Fortell meg-funksjonen](media/ui-search/search_small.png "Fortell hva du vil gjøre"), angi **Ressursgrupper**, og velg deretter den relaterte koblingen.
2. Velg handlingen **Ny**.
3. Fyll ut feltene etter behov.

## <a name="to-set-capacity-for-a-resource"></a>Angi kapasiteten til en ressurs
Hvis du vil beregne hvor mye tid en ressurs kan bruke på prosjekter, må deres kapasitet først defineres som tilgjengelig tid per periode i arbeidskalenderen. Dette oppsettet brukes når du fyller ut prosjetplanleggingslinjer som inneholder ressursen. Hvis du vil ha mer informasjon, kan du se [Opprette prosjekter](projects-how-create-jobs.md).

1. Velg ikonet ![lyspære som åpner Fortell meg-funksjonen](media/ui-search/search_small.png "Fortell hva du vil gjøre"), angi **Ressurser**, og velg deretter den relaterte koblingen.
2. Åpne det aktuelle ressurskortet, og velg deretter handlingen **Ressurskapasitet**.
3. På siden **Ressurskapasitet** i **Vis etter**-feltet, angir du lengden på perioden, for eksempel **Dag**, som vises i kolonner i hurtigfanen **Matrise for ressurskapasitet**.
4. For hver ressurs på en linje angir du for hver periode i kolonnene antall timer som ressursen er tilgjengelig.
5. Hvis du vil angi detaljer om ressursens ukentlige kapasitet innenfor en start- og sluttdato, kan du også velge handlingen **Angi kapasitet**.
6. På siden **Innstillinger for ressurskapasitet** fyller du ut feltene på en linje etter behov.
7. Velg handlingen **Oppdater kapasitet**. Siden **Ressurskapasitet** oppdateres med den angitte kapasiteten.
8. Lukk siden.

## <a name="to-set-up-alternate-resource-costs"></a>Slik definerer du alternative ressurskostpriser
I tillegg til kostprisen som er angitt på ressurskortet, kan du definere alternative kostpriser for hver ressurs. Hvis du for eksempel betaler ansatte en høyere timesats for overtid, kan du definere en ressurskostpris for overtidssatsen. Den alternative kostprisen du definerer for ressursen, overstyrer kostprisen på ressurskortet når du bruker ressursen i ressurskladden.

1. Velg ikonet ![lyspære som åpner Fortell meg-funksjonen](media/ui-search/search_small.png "Fortell hva du vil gjøre"), angi **Ressurser**, og velg deretter den relaterte koblingen.  
2. Velg ressursen som du vil definere ett eller flere alternative kostpriser for, og velg deretter handlingen **Kostpriser**.  
3. På siden **Ressurskostpriser** fyller du ut feltene på en linje etter behov.  
4. Gjenta trinn 3 for hvert alternativ ressurskostpris du vil definere.

**Merk**. Hvis du vil definere ressurskostpriser som skal gjelde for alle ressurser og ressursgrupper, åpner du siden **Ressurskostpriser** og fyller ut feltene.

## <a name="to-set-up-alternate-resource-prices"></a>Slik definerer du alternative ressurspriser
I tillegg til prisen som er angitt på ressurskortet, kan du definere alternative priser for hver ressurs. Disse alternative prisene kan være betinget. De kan være avhengig av at ressursen brukes med et bestemt prosjekt eller arbeidstype.

1. Velg ikonet ![lyspære som åpner Fortell meg-funksjonen](media/ui-search/search_small.png "Fortell hva du vil gjøre"), angi **Ressurser**, og velg deretter den relaterte koblingen.
2. Velg ressursen som du vil definere ett eller flere alternative priser for, og velg deretter handlingen **Priser**.
3. På siden **Ressurspriser** fyller du ut feltene på en linje etter behov.
4. Gjenta trinn 3 for hvert alternativ ressurspris du vil definere.

## <a name="see-also"></a>Se også
[Konfigurere prosjektstyring](projects-setup-projects.md)  
[Prosjektstyring](projects-manage-projects.md)  
[Finans](finance.md)  
[Innkjøp](purchasing-manage-purchasing.md)         
[Salg](sales-manage-sales.md)      
[Arbeide med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)  
