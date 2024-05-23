---
title: Spor forretnings-KPI-ene med Power BI-måleverdier
description: Få en oversikt over hvordan du bruker Power BI til å få forretningsanalyse og KPI-er fra Business Central-data.
author: kennienp
ms.author: kepontop
ms.reviewer: jswymer
ms.topic: overview
ms.search.keywords: 'account schedule, analysis, reporting, financial report, business intelligence, KPI'
ms.search.form: '6316, 6317'
ms.date: 04/24/2024
ms.custom: bap-template
ms.service: dynamics-365-business-central
---

# <a name="track-your-business-kpis-with-power-bi-metrics"></a>Spor forretnings-KPI-ene med Power BI-måleverdier

Hvis du bruker Power BI på [!INCLUDE[prod_short](includes/prod_short.md)]-data, er det enkelt å spore KPI-er eller mål som er viktige for deg.

Med måleverdier i Power BI kan du samle dine egne mål og spore dem mot viktige forretningsmål, i én enkelt rute. Denne funksjonen forbedrer datakulturen ved å fremheve ansvar, justering og synlighet for grupper og initiativer i organisasjoner.

Følg denne firetrinns prosessen for å definere Power BI.-måleverdier:

1. Opprett en målstyring i Power BI. Finn ut mer under [Opprett målstyringer i Power BI](/power-bi/create-reports/service-goals-create).  
2. Legg til måleverdiene du vil spore, ved å koble til Power BI-rapporten om telemetri. Finn ut mer under [Opprett tilkoblede måleverdier](/power-bi/create-reports/service-goals-create-connected).  
3. Legg til varselet, ved behov, ved å definere statusregler for måleverdiene. Finn ut mer under [Opprett automatiserte statusregler for måleverdier](/power-bi/create-reports/service-metrics-status-rules).  

    Dette trinnet automatiserer statusoppdateringer basert på regler som styrer måleverdien. Regler utløser endringer basert på verdi, prosent av mål oppfylt, datobetingelser eller en kombinasjon av de tre, slik at reglene blir fleksible. For tilkoblede måleverdier oppdateres disse statusreglene hver gang dataene i målstyringen oppdateres.
4. Følg måleverdier for å hente varsler i Teams eller via e-post. Finn ut mer under [Følg måleverdiene](/power-bi/create-reports/service-metrics-follow).  

Finn ut mer om Power BI-måleverdier under [Kom i gang med måleverdier i Power BI](/power-bi/create-reports/service-goals-introduction).

> [!NOTE]
> Fra og med lanseringsbølge 2 for 2023 for Business Central er det mulig å bygge inn målstyringer fra Power BI-måledata i [!INCLUDE[prod_short](includes/prod_short.md)].

## <a name="see-also"></a>Se også

[Bruk ytelsesindikatorer (KPI-er) til å oppfylle forretningsmålene](analytics-about-kpis.md)  
[Innføring i Business Central og Power BI](admin-powerbi.md)  
[Arbeid med Power BI-rapporter](across-working-with-powerbi.md)  
[Oversikt over analyse](reports-bi-reporting.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
