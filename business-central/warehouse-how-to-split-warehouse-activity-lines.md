---
title: Dele lageraktivitetslinjer | Microsoft-dokumentasjon
description: "I plasseringer, flyttinger eller plukkinger og i lagerplasseringer og lagerplukkinger foreslås det hyller for plukking eller plassering av varer. Det kan hende at det faktiske antallet i den foreslåtte hyllen ikke er tilstrekkelig, eller at det ikke er nok plass i den foreslåtte hyllen til å plassere det nødvendige antallet. I slike tilfeller må du dele linjen, slik at varene på en linje blir hentet fra eller plassert i flere enn én hylle."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 08/16/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: d7fb34e1c9428a64c71ff47be8bcff174649c00d
ms.openlocfilehash: dfb633ef874b77a3cf6060311f0bcbbf66e05102
ms.contentlocale: nb-no
ms.lasthandoff: 03/22/2018

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
[Arbeide med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

