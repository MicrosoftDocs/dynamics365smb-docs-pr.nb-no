---
title: Slik massebokfører du produksjonsavgang og operasjonstider | Microsoft-dokumentasjon
description: Avgangsantallet representerer arbeidsframdriften i form av det ferdige antallet.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/01/2019
ms.author: sgroespe
ms.openlocfilehash: cc4acf5fbaf10df3b833e310a83854e52b0d2b73
ms.sourcegitcommit: 02e704bc3e01d62072144919774f1244c42827e4
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 10/01/2019
ms.locfileid: "2313255"
---
# <a name="batch-post-output-and-run-times"></a>Bokføre avgang og operasjonstid
Avgangsantallet representerer arbeidsframdriften i form av det ferdige antallet.  

> [!NOTE]
> Bare når du bokfører avgangsantall i den siste operasjonen, oppdateres beholdningen automatisk.  

## <a name="to-post-output-quantities-for-one-or-more-production-order-lines"></a>Slik bokfører du avgangsantall for en eller flere produksjonsordrelinjer
1. Velg ikonet ![lyspære som åpner Fortell meg-funksjonen](media/ui-search/search_small.png "Fortell hva du vil gjøre"), angi **Ferdigmeldingskladd**, og velg deretter den relaterte koblingen.  
2. Fyll ut feltene med produksjonsordre- og avgangsdata. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
3. Hvis operasjonen er fullført, velger du **Ferdig**-feltet.  

    Hvis lagerlokasjonen der varene skal plasseres bruker hyller, men ikke krever plasseringsbehandling,  tildeler du en hyllekode til kladdelinjen for å angi hvor varene skal lagres på lageret Hvis du vil ha mer informasjon, kan du se [Plassere produksjonsavgang eller monteringsavgang](warehouse-how-to-put-away-production-output.md).  

4. Velg **Bokfør** for å bokføre operasjonene. Avgangsantallet bokføres. Varen kan nå leveres.  

## <a name="to-post-run-times-for-one-or-more-production-order-lines"></a>Slik bokfører du kjøretid for en eller flere produksjonsordrelinjer
Operasjonstiden representerer arbeidsframdrift i form av nødvendig arbeidstid.    

1.  Velg ikonet ![lyspære som åpner Fortell meg-funksjonen](media/ui-search/search_small.png "Fortell hva du vil gjøre"), angi **Ferdigmeldingskladd**, og velg deretter den relaterte koblingen.  
2. Fyll ut feltene med produksjonsordre- og avgangsdata.  
3.  Hvis operasjonen er fullført, velger du **Ferdig**-feltet.  
4. Velg **Bokfør**-handlingen for å bokføre tiden som brukes per operasjon. Kapasitetsposter oppdateres for brukte arbeids- eller produksjonsressurser.

## <a name="see-also"></a>Se også  
[Produksjon](production-manage-manufacturing.md)    
[Definere produksjon](production-configure-production-processes.md)  
[Planlegging](production-planning.md)      
[Lager](inventory-manage-inventory.md)  
[Innkjøp](purchasing-manage-purchasing.md)  
[Arbeide med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)
