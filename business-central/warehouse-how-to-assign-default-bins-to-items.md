---
title: Tilordne standardhyller til varer
description: Hvis du bruker hyller i en lokasjon, kan du tilordne standardhyller til varene for å gjøre levering, mottak og flytting av varene enklere.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 06/25/2021
ms.author: edupont
ms.openlocfilehash: 05d338234bbb4a6c578935c8aa29e32f9453f615
ms.sourcegitcommit: a7cb0be8eae6ece95f5259d7de7a48b385c9cfeb
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 07/08/2021
ms.locfileid: "6445875"
---
# <a name="assign-default-bins-to-items"></a>Tilordne standardhyller til varer
Hvis du bruker hyller i en lokasjon, kan du tilordne standardhyller til varene for å gjøre levering, mottak og flytting av varene enklere. Når en standardhylle tilordnes en vare, foreslås denne hyllen hver gang du oppretter en transaksjon for denne varen. Standardhyller defineres på siden **Hylleinnhold**.  

## <a name="to-assign-a-default-bin-to-an-item"></a>Tilordne en standardhylle til en vare
1.  Velg ikonet ![Lyspære som åpner funksjonen Fortell meg.](media/ui-search/search_small.png "Fortell hva du vil gjøre") og skriv inn **Hylleinnholdopprett. – forslag**, og velg deretter den relaterte koblingen.  
2.  Fyll ut hyllekoden og opplysninger om varen for hver hylle du vil definere som standard for en vare. Pass på å velge **Standard**-feltet.  
3.  Velg **Opprett hylleinnhold**-handlingen. Standardhyllene tilordnes for varen.  

> [!NOTE]  
>  Hvis en vare ikke er tilordnet en standardhylle når den plasseres, vil hyllen der varen plasseres, tilordnes som standardhylle.  

## <a name="to-change-the-default-bin-for-an-item"></a>Slik endrer du standardhyllen for en vare  
Det kan hende du må endre tilordningen av standardhylle for en vare eller tilordne en standardhylle til en ny vare.    
1.  Velg ikonet ![Lyspære som åpner funksjonen Fortell meg.](media/ui-search/search_small.png "Fortell hva du vil gjøre") og angi **Hylleinnhold** og velg den relaterte koblingen.  
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
[Arbeide med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]