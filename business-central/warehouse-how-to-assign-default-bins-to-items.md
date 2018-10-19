---
title: Tilordne standardhyller til varer | Microsoft-dokumentasjon
description: "Hvis du bruker hyller i en lokasjon, kan du tilordne standardhyller til varene for å gjøre levering, mottak og flytting av varene enklere. Når en standardhylle tilordnes en vare, foreslås denne hyllen hver gang du oppretter en transaksjon for denne varen."
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
ms.sourcegitcommit: 9dbd92409ba02281f008246194f3ce0c53e4e001
ms.openlocfilehash: e6c6c8a54ae638fa90bca94e43a38d120b5fd3f6
ms.contentlocale: nb-no
ms.lasthandoff: 09/28/2018

---
# <a name="assign-default-bins-to-items"></a>Tilordne standardhyller til varer
Hvis du bruker hyller i en lokasjon, kan du tilordne standardhyller til varene for å gjøre levering, mottak og flytting av varene enklere. Når en standardhylle tilordnes en vare, foreslås denne hyllen hver gang du oppretter en transaksjon for denne varen. Standardhyller defineres i vinduet **Hylleinnhold**.  

## <a name="to-assign-a-default-bin-to-an-item"></a>Tilordne en standardhylle til en vare
1.  Velg ikonet ![lyspære som åpner Fortell meg-funksjonen](media/ui-search/search_small.png "Fortell hva du vil gjøre"), angi **Forslag for oppretting av hylleinnhold**, og velg deretter den relaterte koblingen.  
2.  Fyll ut hyllekoden og opplysninger om varen for hver hylle du vil definere som standard for en vare. Pass på å velge **Standard**-feltet.  
3.  Velg **Opprett hylleinnhold**-handlingen. Standardhyllene tilordnes for varen.  

> [!NOTE]  
>  Hvis en vare ikke er tilordnet en standardhylle når den plasseres, vil hyllen der varen plasseres, tilordnes som standardhylle.  

## <a name="to-change-the-default-bin-for-an-item"></a>Slik endrer du standardhyllen for en vare  
Det kan hende du må endre tilordningen av standardhylle for en vare eller tilordne en standardhylle til en ny vare.    
1.  Velg ikonet ![lyspære som åpner Fortell meg-funksjonen](media/ui-search/search_small.png "Fortell hva du vil gjøre"), angi **Hylleinnhold**, og velg deretter den relaterte koblingen.  
2.  I feltet **Lokasjonsfilter** velger du den riktige lokasjonskoden.  
3.  Finn den gjeldende posten med standard hylleinnhold for varen, og fjern avmerkingen for **Standardhylle**.  
4.  Finn hylleinnholdslinjen for hyllen som du vil bruke som ny standardhylle. Merk av for **Standardhylle**.  

> [!NOTE]  
>  Hvis en vare ikke er tilordnet en standardhylle når den plasseres første gang, vil systemet tilordne hyllen der varen plasseres, som standardhylle.  

## <a name="see-also"></a>Se også  
[Lagerstyring](warehouse-manage-warehouse.md)  
[Lager](inventory-manage-inventory.md)  
[Definere lagerstyring](warehouse-setup-warehouse.md)     
[Monteringsstyring](assembly-assemble-items.md)    
[Designdetaljer: Lagerstyring](design-details-warehouse-management.md)  
[Arbeide med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

