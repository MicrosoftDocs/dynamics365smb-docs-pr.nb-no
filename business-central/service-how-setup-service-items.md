---
title: Oppsett av servicevarer og servicevarekomponenter | Microsoft-dokumentasjon
description: Finn ut mer om ting du må definere før du kan bruke servicevarer, inkludert standardverdier som responstid, kontraktrabattprosent og serviceprisgruppe.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/01/2018
ms.author: sgroespe
ms.openlocfilehash: e82aa86668da5999117eea636ee29d8fde2cc09e
ms.sourcegitcommit: 1bcfaa99ea302e6b84b8361ca02730b135557fc1
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 03/08/2019
ms.locfileid: "803199"
---
# <a name="set-up-service-items-and-service-item-components"></a>Definere servicevarer og servicevarekomponenter
Hvis du vil arbeide med servicevarer, må du definere følgende

* Servicevaregrupper.
* Valgfritt

## <a name="to-set-up-service-item-groups"></a>Definere servicevaregrupper
Du kan angi grupper av varer som er relaterte med hensyn til reparasjon og vedlikehold. Du kan definere standardverdier for servicevarer i en servicevaregruppe, for eksempel responstid, kontraktrabattprosent og serviceprisgruppe. For varer i en servicevaregruppe kan du velge om du vil at de skal registreres automatisk som servicevarer når de selges.  

Du tilordner servicevaregrupper til varer **Vare**-kortet og servicevarer på **Servicevare**-kortet.  

1. Velg ikonet ![lyspære som åpner Fortell meg-funksjonen](media/ui-search/search_small.png "Fortell hva du vil gjøre"), angi **Servicevaregrupper**, og velg deretter den relaterte koblingen.  
2. Opprett en ny servicevaregruppe.  
3. Fyll ut feltene **Kode** og **Beskrivelse**.  
4. I feltet **Standard kontraktrabatt-%** angir du den standard kontraktrabattprosenten som du vil at servicevarene i gruppen skal ha.  
5. I feltet **Standard serv.prisgruppekode** angir du den standard serviceprisgruppekoden som du vil at servicevarene i gruppen skal ha.  
6. I feltet **Standard responstid (timer)** angir du den standard responstiden i timer som du vil at servicevarene i gruppen skal ha.  
7. Hvis du vil registrere varene i gruppen som servicevarer når de selges, velger du feltet **Opprett servicevare**.  

## <a name="to-set-up-service-item-components"></a>Slik definerer du servicevarekomponenter
En servicevare kan bestå av flere komponenter, som kan erstattes med reservedeler når varen vedlikeholdes. Disse komponentene defineres på siden **Oversikt over servicevarekomponenter**. Hvis du vil definere komponenter for servicevarer som er stykklister, kan du også kopiere stykklistevarene, og deretter opprette dem som servicevarekomponenter.

1. Velg ikonet ![lyspære som åpner Fortell meg-funksjonen](media/ui-search/search_small.png "Fortell hva du vil gjøre"), angi **Servicevarer**, og velg deretter den relaterte koblingen.
2. Åpne servicevaren du vil definere komponenter for.  
3. Velg handlingen **Komponenter**. Siden **Oversikt over servicevarekomponenter** åpnes.  
4. Legg til en ny komponent.  
5. I **Type**-feltet velger du **Servicevare** hvis selve komponenten er en registrert servicevare. Ellers velger du **Vare**.  
6. I feltet **Nr.** -feltet velger du varen eller servicevaren som er en komponent i servicevaren.  

## <a name="to-set-up-service-item-components-from-a-bom"></a>Slik definerer du servicevarekomponenter fra stykklister
1.  Velg ikonet ![lyspære som åpner Fortell meg-funksjonen](media/ui-search/search_small.png "Fortell hva du vil gjøre"), angi **Servicevarer**, og velg deretter den relaterte koblingen.  
2. Åpne servicevaren du vil definere komponenter fra en stykkliste for.  
3. Velg handlingen **Komponenter**. Siden **Oversikt over servicevarekomponenter** åpnes.  
4. Velg handlingen **Kopier fra stykkliste**.  

    Hvis varen som servicevaren er knyttet til, er en stykkliste, opprettes komponentene for alle varene i stykklisten automatisk.  

## <a name="to-set-up-a-service-shelf"></a>Slik definerer du servicehyller
Du kan definere servicehyller som identifiserer hvor du lagrer servicevarene. Du tilordner servicehyller til servicevarer på sidene **Serviceordre** og **Servicevareskjema**.  

1. Velg ikonet ![lyspære som åpner Fortell meg-funksjonen](media/ui-search/search_small.png "Fortell hva du vil gjøre"), angi **Servicehyller**, og velg deretter den relaterte koblingen.
2. Fyll ut feltene etter behov.

## <a name="see-also"></a>Se også
[Definere koder for standardservicer](service-how-setup-service-coding.md)   
[Definere feilsøking](service-how-setup-troubleshooting.md)
