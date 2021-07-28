---
title: Dele lageraktivitetslinjer
description: Les hvordan du deler lageraktivitetslinjer hvis den disponible kapasiteten i en foreslått hylle ikke er tilstrekkelig.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 06/25/2021
ms.author: edupont
ms.openlocfilehash: 46ac47dbf3b1df3f89b83c56215831100edb3827
ms.sourcegitcommit: e562b45fda20ff88230e086caa6587913eddae26
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 06/30/2021
ms.locfileid: "6325246"
---
# <a name="split-warehouse-activity-lines"></a>Dele lageraktivitetslinjer
I plasseringer, flyttinger eller plukkinger og i lagerplasseringer og lagerplukkinger foreslås det hyller for plukking eller plassering av varer. Det kan hende at det faktiske antallet i den foreslåtte hyllen ikke er tilstrekkelig, eller at det ikke er nok plass i den foreslåtte hyllen til å plassere det nødvendige antallet. I slike tilfeller må du dele linjen, slik at varene på en linje blir hentet fra eller plassert i flere enn én hylle.  

Følgende fremgangsmåte gjelder for lagerdokumenter , for eksempel plassering, flytting og plukklinjer, eller lagerplassering, flytting og plukklinjer.  

## <a name="to-split-warehouse-activity-lines"></a>Slik deler du lageraktivitetslinjer:  
1.  Åpne en lageraktivitetslinje hvor du prøver å håndtere et utilstrekkelig antall.  
2.  Angi det reduserte antallet du kan håndtere, i feltet **Ant. som skal håndt.**.  
3.  På hurtigfanen **Linjer** velger du handlingen **Handlinger**, **Funksjoner**, og deretter **Del linje**. Det vises en ny linje som er en kopi av den opprinnelige linjen, bortsett fra at feltet **Ant. som skal håndt.** inneholder antallet du fjernet fra den opprinnelige linjen.  
4.  Tilordne den aktuelle hyllen og, hvis du bruker lagerstyring, sonen, til den nye linjen, eller del eventuell linjen flere ganger til du finner hyller til alle antallene.  

> [!NOTE]  
>  Hvis lokasjonen bruker lagerstyring og du deler linjene, må du være kjent med lageret, og du må være i stand til å velge en hylle som samsvarer med lagringskravene for varen, og som oppfyller de generelle kravene i lagerdokumentet. Du bør for eksempel ikke dele en linje i et plukkdokument og plasser noen varer i masselagringen.  

## <a name="see-also"></a>Se også  
[Lagerstyring](warehouse-manage-warehouse.md)  
[Lager](inventory-manage-inventory.md)  
[Definere lagerstyring](warehouse-setup-warehouse.md)     
[Monteringsstyring](assembly-assemble-items.md)    
[Designdetaljer: Lagerstyring](design-details-warehouse-management.md)  
[Arbeide med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]