---
title: Anbefalte fremgangsmåter for globalt planleggingsoppsett | Microsoft-dokumentasjon
description: Hurtigfanen Planlegging på siden Produksjonsoppsett inneholder flere felt som definerer globale regler for forsyningsplanlegging.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/01/2021
ms.author: edupont
ms.openlocfilehash: c91bde42378992ef1c1e9613fb94d9bac2d4f57c
ms.sourcegitcommit: 766e2840fd16efb901d211d7fa64d96766ac99d9
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 03/31/2021
ms.locfileid: "5785351"
---
# <a name="setup-best-practices-global-planning-setup"></a>Anbefalte fremgangsmåter for oppsett: Oppsett for global planlegging
Hurtigfanen **Planlegging** på siden **Produksjonsoppsett** inneholder flere felt som definerer globale regler for forsyningsplanlegging.  

 Tabellen nedenfor inneholder anbefalte fremgangsmåter for hvordan du konfigurerer valgte globale planleggingsparameterfelt. Hvis du vil ha mer informasjon om et felt, velger du koblingen i kolonnen **Oppsettfelt**.  

|Oppsettfelt|Anbefalt fremgangsmåte|Merknad|  
|-----------------|-------------------|-------------|  
|Bruk prognose på lokasjoner|Velg dette alternativet hvis du har prognoser for bestemte plasseringer.||  
|Komponenter ved lokasjon|Hvis varene ikke er definert som lagerføringsenheter, velger du lokasjonskoden for hovedlageret.|Dette gjelder også hvis du bare bruker bestillingsforslaget.|  
|Tomt overflytnivå|Velg **Tillat standardberegning** hvis du migrerer fra Microsoft Dynamics NAV 5.0 eller tidligere.|Bruk bare hvis du vil tillate at alle eller noen av varene flyter over gjenbestillingspunktet.|  
|Standard avdempingsperiode|Velg mellom 1D og 5D.<br /><br /> Hvis planlegging er nytt for brukerne i [!INCLUDE[prod_short](includes/prod_short.md)], angir du en lengre periode.|Når brukere har satt seg bedre inn i de forskjellige årsakene til handlingsmeldinger, kan avdempingsperioden forkortes for å tillate flere endringsforslag.|  
|Standard avdempingsantall %|Angi mellom 5 og 20 prosent av varens partistørrelse.||  

## <a name="see-also"></a>Se også  
 [Anbefalte fremgangsmåter for oppsett: Forsyningsplanlegging](setup-best-practices-supply-planning.md)   
 [Designdetaljer: Forsyningsplanlegging](design-details-supply-planning.md)   
 [Konfigurere komplekse moduler ved å bruke anbefalte fremgangsmåter](set-up-complex-application-areas-using-best-practices.md)  
 [Arbeide med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]