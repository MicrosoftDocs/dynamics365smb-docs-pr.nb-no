---
title: Definere plasseringsmaler | Microsoft-dokumentasjon
description: Med funksjonaliteten for lagerstyring foreslås den hyllen som passer best til varene på et hvilket som helst tidspunkt, i henhold til den plasseringsmalen du har definert for lageret, de hylleprioriteringene du har gitt til hyllene, og de minimums- og maksimumsantallene du har definert for faste hyller.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/01/2019
ms.author: sgroespe
ms.openlocfilehash: 811e3cda680d414694f1cf060bdb66390939e6d6
ms.sourcegitcommit: cfc92eefa8b06fb426482f54e393f0e6e222f712
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 12/03/2019
ms.locfileid: "2876399"
---
# <a name="set-up-put-away-templates"></a>Definere plasseringsmaler
Med funksjonaliteten for lagerstyring foreslås den hyllen som passer best til varene på et hvilket som helst tidspunkt, i henhold til den plasseringsmalen du har definert for lageret, de hylleprioriteringene du har gitt til hyllene, og de minimums- og maksimumsantallene du har definert for faste hyller.  

Du kan definere flere plasseringsmaler og velge én av dem som i hovedsak skal styre plasseringene i lageret. Du kan også velge en plasseringsmal for en hvilken som helst vare eller lagerføringsenhet som kan ha spesielle plasseringskrav.  

## <a name="to-set-up-put-away-templates"></a>Slik setter du opp plasseringsmaler  
1.  Velg ikonet ![lyspære som åpner Fortell meg-funksjonen](media/ui-search/search_small.png "Fortell hva du vil gjøre"), angi **Plasseringsmaler**, og velg deretter den relaterte koblingen.  
2.  Velg handlingen **Ny**.  
3.  Angi en kode som er den unike identifikatoren for malen du er i ferd med å opprette.  
4.  Hvis du vil, kan du angi en kort beskrivelse.  
5.  Fyll ut den første linjen med de hyllekravene du først og fremst vil skal oppfylles når en plassering foreslås.  
6.  Fyll ut den andre linjen med hyllekravene som skal være ditt andrevalg å oppfylle når en hylle blir funnet for plasseringen. Den andre linjen brukes bare hvis det ikke blir funnet en hylle som oppfyller kravene på den første linjen.  
7.  Fortsett med å fylle ut linjene til du har beskrevet alle de akseptable hylleplasseringene du vil bruke i plasseringsprosessen.  
8.  På den siste linjen i plasseringsmalen merker du av for **Finn flytende hylle**.  

Du kan opprette forskjellige plasseringsmaler og deretter bruke dem slik det passer. Plasseringsmalen du har valgt for varen eller lagerføringsenheten, brukes først, hvis du har valgt en mal. Hvis disse feltene ikke er utfylt, brukes plasseringsmalen du valgte for lageret på hurtigfanen **Hylleprinsipp** på lokasjonskortet.  

## <a name="see-also"></a>Se også  
[Lagerstyring](warehouse-manage-warehouse.md)  
[Lager](inventory-manage-inventory.md)  
[Definere lagerstyring](warehouse-setup-warehouse.md)     
[Monteringsstyring](assembly-assemble-items.md)    
[Designdetaljer: Lagerstyring](design-details-warehouse-management.md)  
[Arbeide med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)
