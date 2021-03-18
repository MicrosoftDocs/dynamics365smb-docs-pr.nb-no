---
title: Definere lokasjoner slik at de bruker hyller | Microsoft-dokumentasjon
description: Hyller representerer den enkle lagerstrukturen og brukes til å komme med forslag om plasseringen av varer. Når du har opprettet hyllene, kan du definere det innholdet du vil plassere i hver hylle, svært spesifikt, eller hyllen kan fungere som en mobil hylle uten angitt innhold.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: 26f6898cbcb63f19ea3b89d5cd1e5df254bc33af
ms.sourcegitcommit: ff2b55b7e790447e0c1fcd5c2ec7f7610338ebaa
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 02/15/2021
ms.locfileid: "5382380"
---
# <a name="set-up-locations-to-use-bins"></a>Definere lokasjoner slik at de bruker hyller
Hyller representerer den enkle lagerstrukturen og brukes til å komme med forslag om plasseringen av varer. Når du har opprettet hyllene, kan du definere det innholdet du vil plassere i hver hylle, svært spesifikt, eller hyllen kan fungere som en mobil hylle uten angitt innhold.  

Når du skal bruke hyllen funksjonelt på en lokasjon, må du først aktivere funksjonaliteten på **Lokasjon**-kortet. Du utformer deretter vareflyten på lokasjonen ved å angi hyllekoder i oppsettsfeltene som representerer ulike flyter.  

> [!NOTE]  
>  Før du kan angi hyllekoder på lokasjonskortet, må hyllekodene være opprettet. Hvis du vil ha mer informasjon, kan du se [Opprette hyller](warehouse-how-to-create-individual-bins.md).  

## <a name="to-set-up-a-location-to-use-bins"></a>Sette opp en lokasjon til å bruke hyller  
1.  Velg ikonet ![lyspære som åpner Fortell meg-funksjonen](media/ui-search/search_small.png "Fortell hva du vil gjøre"), angi **Lokasjoner**, og velg deretter den relaterte koblingen.  
2.  Velg lokajonen der du vil bruke hyller.  
3.  Velg handlingen **Rediger**.  
4.  På hurtigfanen **Lager** merker du av for **Hylle obligatorisk**.  
5.  Hvis du ikke bruker lagerstyring for lokasjonen, fyller du ut feltet **Standard hyllevalg** med metoden systemet skal bruke til å tilordne en standardhylle til en vare.  
6.  Åpne kortet for lokasjonen du vil konfigurere hyller for.
7.  På hurtigfanen **Hyller** velger du de hyllene du vil bruke som standard for mottak og leveringer og inngående, utgående og åpne produksjonshyller.  
8.  De hyllekodene du angir her, vil bli vist automatisk i hodene og på linjene i ulike lagerdokumenter. Standardhyllene definerer alle start- og sluttplasseringer for varene i lageret.  
9.  Hvis du bruker lagerstyring, velger du en hylle til lagerjusteringer. Hyllekoden i feltet **Hyllekode for justering** definerer den virtuelle hyllen som skal registrere avvik i beholdning når du registrerer enten observerte forskjeller som er registrert i lagerets varekladd, eller forskjeller som beregnes når du registrerer en lageropptelling.  
10. Fyll ut feltene i hurtigfane **Hylleprinsipp** hvis de er relevante for lageret. De viktigste feltene er **Hyllekapasitetsprinsipp**, **Tillat anbrekk** og **Plasseringsmal - kode**.  
11. På hurtigfanen **Lager** fyller du ut feltene **Utgående lagerhåndteringstid**, **Inngående lagerhåndteringstid** og **Hovedkalenderkode**. Hvis du vil ha mer informasjon, kan du se [Definere hovedkalendere](across-how-to-assign-base-calendars.md).

## <a name="filling-the-consumption-bin"></a>Fylle forbrukshyllen
Dette flytdiagrammet viser hvordan **Hyllekode**-feltet på produksjonsordrekomponentlinjer fylles ut i henhold til lokasjonsoppsettet.

![Flytskjema for hylle](media/binflow.png "BinFlow")  

## <a name="see-also"></a>Se også
[Lagerstyring](warehouse-manage-warehouse.md)  
[Lager](inventory-manage-inventory.md)  
[Definere lagerstyring](warehouse-setup-warehouse.md)     
[Monteringsstyring](assembly-assemble-items.md)    
[Designdetaljer: Lagerstyring](design-details-warehouse-management.md)  
[Arbeide med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]