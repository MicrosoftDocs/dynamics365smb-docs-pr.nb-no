---
title: "Definere lagerføringsenheter | Microsoft-dokumentasjon"
description: "Du kan bruke lagerføringsenheter til å registrere opplysninger om varer for en bestemt lokasjon eller en bestemt variantkode."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 08/23/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 2c13559bb3dc44cdb61697f5135c5b931e34d2a8
ms.openlocfilehash: e5ac1c791b10c26a3cecd20711e7899bb7eaee3c
ms.contentlocale: nb-no
ms.lasthandoff: 09/22/2017

---
# Definere lagerføringsenheter
Du kan bruke lagerføringsenheter til å registrere opplysninger om varer for en bestemt lokasjon eller en bestemt variantkode.  

 Lagerføringsenheter er et tillegg til varekort. De erstatter dem ikke, selv om de er knyttet til dem. Med lagerføringsenheter kan du skille mellom opplysninger om en vare for en bestemt lokasjon (for eksempel et lager eller et distribusjonssenter) eller en bestemt variant (for eksempel ulike hyllenumre og ulike opplysninger om etterfylling), for den samme varen.  

## Slik definerer du lagerføringsenheter  

1.  Velg ikonet ![Søk etter side eller rapport](media/ui-search/search_small.png "Ikonet Søk etter side eller rapport"), angi **Lagerføringsenheter**, og velg deretter den relaterte koblingen.  
2.  Velg handlingen **Ny**.  
3.  Fyll ut feltene på kortet. Følgende felt er obligatoriske: **Varenr.**, **Lokasjonskode** og/eller **Variantkode**. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]  

Når du har definert den første lagerføringsenheten for en vare, blir det merket av for **Lagerføringsenhet** på **vare** kortet.  

Hvis du vil opprette flere lagerføringsenheter for en vare, bruker du kjørselen **Opprett lagerføringsenhet**.  

> [!NOTE]  
>  Opplysningene på **lagerføringsenhetskortet** har høyere prioritet enn opplysningene på **varekortet**.  

## Se også  
[Registrere nye varer](inventory-how-register-new-items.md)  
[Definere lagerstyring](warehouse-setup-warehouse.md)  
[Lagerstyring](warehouse-manage-warehouse.md)  
[Lager](inventory-manage-inventory.md)  
[Monteringsstyring](assembly-assemble-items.md)    
[Designdetaljer: Lagerstyring](design-details-warehouse-management.md)  
[Arbeide med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)  

