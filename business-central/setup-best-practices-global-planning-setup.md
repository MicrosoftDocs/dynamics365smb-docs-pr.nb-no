---
title: Anbefalte fremgangsmåter for globalt planleggingsoppsett | Microsoft-dokumentasjon
description: Hurtigfanen Planlegging på siden Produksjonsoppsett inneholder flere felt som definerer globale regler for forsyningsplanlegging.
author: brentholtorf
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: null
ms.date: 04/01/2021
ms.author: bholtorf
---
# Anbefalte fremgangsmåter for oppsett: Oppsett for global planlegging
Hurtigfanen **Planlegging** på siden **Produksjonsoppsett** inneholder flere felt som definerer globale regler for forsyningsplanlegging.  

 Tabellen nedenfor inneholder anbefalte fremgangsmåter for hvordan du konfigurerer valgte globale planleggingsparameterfelt. Hvis du vil ha mer informasjon om et felt, velger du koblingen i kolonnen **Oppsettfelt**.  

|Oppsettfelt|Anbefalt fremgangsmåte|Merknad|  
|-----------------|-------------------|-------------|  
|Bruk prognose på lokasjoner|Velg dette alternativet hvis du har prognoser for bestemte plasseringer.||  
|Komponenter ved lokasjon|Hvis varene ikke er definert som lagerføringsenheter, velger du lokasjonskoden for hovedlageret.|Dette gjelder også hvis du bare bruker bestillingsforslaget.|  
|Tomt overflytnivå|Velg **Tillat standardberegning** hvis du migrerer fra Microsoft Dynamics NAV 5.0 eller tidligere.|Bruk bare hvis du vil tillate at alle eller noen av varene flyter over gjenbestillingspunktet.|  
|Standard avdempingsperiode|Velg mellom 1D og 5D.<br /><br /> Hvis planlegging er nytt for brukerne i [!INCLUDE[prod_short](includes/prod_short.md)], angir du en lengre periode.|Når brukere har satt seg bedre inn i de forskjellige årsakene til handlingsmeldinger, kan avdempingsperioden forkortes for å tillate flere endringsforslag.|  
|Standard avdempingsantall %|Angi mellom 5 og 20 prosent av varens partistørrelse.||  

## Se også  
 [Anbefalte fremgangsmåter for oppsett: Forsyningsplanlegging](setup-best-practices-supply-planning.md)   
 [Designdetaljer: Forsyningsplanlegging](design-details-supply-planning.md)   
 [Konfigurere komplekse moduler ved å bruke anbefalte fremgangsmåter](set-up-complex-application-areas-using-best-practices.md)  
 [Arbeid med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]