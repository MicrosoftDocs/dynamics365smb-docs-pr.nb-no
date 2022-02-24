---
title: Flytte varer | Microsoft-dokumentasjon
description: Varer som er på lager, må kanskje flyttes mellom hyller for å opprettholde vareflyten gjennom lageret. Noen flyttinger skjer i direkte tilknytning til interne operasjoner, for eksempel en produksjonsordre som trenger komponenter levert eller sluttvarer plassert. Andre flyttinger skjer som ren lagerplassoptimalisering eller ad-hoc flyttinger til og fra operasjoner.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/01/2019
ms.author: sgroespe
ms.openlocfilehash: f7fd88c88a69806e6cc914c27737d3a8b823bc51
ms.sourcegitcommit: cfc92eefa8b06fb426482f54e393f0e6e222f712
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 12/03/2019
ms.locfileid: "2876491"
---
# <a name="moving-items"></a>Flytte varer
Lageraktiviteten med å flytte varer i lageret utføres på ulike måter avhengig av hvordan lagerstyringsfunksjonene er satt opp. Kompleksiteten kan variere fra ingen lagerfunksjoner, via grunnleggende lagerkonfigurasjoner der bestilling for bestilling behandles ved hjelp av bare en eller flere aktiviteter, til avanserte oppsett der alle lageraktiviteter utføres i en styrt arbeidsflyt. Du finner mer informasjon under [Definere lagerstyring](warehouse-setup-warehouse.md).

Varer som er på én lagerlokasjon, må kanskje flyttes mellom hyller for å opprettholde vareflyten gjennom lageret. Noen flyttinger skjer i direkte tilknytning til interne operasjoner, for eksempel en produksjonsordre som trenger komponenter levert eller sluttvarer plassert. Andre flyttinger skjer som ren lagerplassoptimalisering eller ad-hoc flyttinger til og fra operasjoner.

Andre flytteoppgaver er å etterfylle plukkhyller og åpne produksjonshyller jevnlig, og å endre informasjonen om hylleinnhold.

Flytting av varer til andre lokasjoner påvirker varepostene, og dette må derfor gjøres ved hjelp av en overføringsordre. Hvis du vil ha mer informasjon, kan du se [Overføre beholdning mellom lokasjoner](inventory-how-transfer-between-locations.md).  

De lagerrelaterte oppgavene med å telle, justere og reklassifisere varene kan omfatte lagerppgaver som må utføres i lagerpostene før de kan synkroniseres med de relaterte varepostene. Hvis du vil ha mer informasjon, se [Telle, justere og reklassifisere lagerbeholdning](inventory-how-count-adjust-reclassify.md)  

 Tabellen nedenfor beskriver en sekvens av oppgaver, og har koblinger til emnene som beskriver dem.   

|**Hvis du vil**|**Se**|  
|------------|-------------|  
|Flytte varer mellom hyller i enkle lageroppsett når som helst og uten kildedokumenter.|[Flytte varer i enkle lageroppsett](warehouse-how-to-move-items-ad-hoc-in-basic-warehousing.md)|
|Bruk lagerflytteforslaget til å flytte varer i avanserte lageroppsett, både for kildedokumenter og ad hoc.|[Flytte varer i avanserte lageroppsett](warehouse-how-to-move-items-in-advanced-warehousing.md)|  
|Ta med komponentvarer for interne operasjoner i grunnleggende lagerkonfigurasjoner som forespurt av kildedokumenter for disse operasjonene.|[Flytte komponenter til et operasjonsområde i enkle lageroppsett](warehouse-how-to-move-components-to-an-operation-area-in-basic-warehousing.md)|
|Planlegge hvilke hyller som skal fylles eller tømmes for å opprettholde en effektiv flyt, for eksempel planlegge tømming av et masselagringsområde før et stort mottak.|[Planlegge lagerflyttinger i forslag](warehouse-how-to-plan-warehouse-movements-in-worksheets.md)|
|Oppdatere hvor hyppig hyllene (for eksempel plukkhyller) må fylles på grunn av svingninger i etterspørsel.|[Beregn etterfylling av hylle](warehouse-how-to-calculate-bin-replenishment.md)|
|Omstrukturer lageret med nye hyllekoder og nye hylleegenskaper og flytt dem eventuelt rundt.|[Omstrukturere lagre](warehouse-how-to-restructure-warehouses.md)|  

## <a name="see-also"></a>Se også  
[Lagerstyring](warehouse-manage-warehouse.md)  
[Lager](inventory-manage-inventory.md)  
[Definere lagerstyring](warehouse-setup-warehouse.md)     
[Monteringsstyring](assembly-assemble-items.md)    
[Designdetaljer: Lagerstyring](design-details-warehouse-management.md)  
[Arbeide med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)
