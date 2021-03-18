---
title: Vise egendefinerte Power BI-rapporter for Business Central-data | Microsoft Docs
description: Du kan bruke Power BI-rapporter til å få ytterligere innsikt i data i lister.
author: jswymer
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: business intelligence, KPI, Odata, Power App, SOAP, analysis
ms.date: 10/01/2020
ms.author: jswymer
ms.openlocfilehash: 6c818940357ed21a994e7553517989a0c16accec
ms.sourcegitcommit: ff2b55b7e790447e0c1fcd5c2ec7f7610338ebaa
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 02/15/2021
ms.locfileid: "5379276"
---
# <a name="creating-power-bi-reports-for-displaying-list-data-in-prod_short"></a>Opprette Power BI-rapporter for å vise listedata i [!INCLUDE[prod_short](includes/prod_short.md)]

[!INCLUDE[prod_long](includes/prod_long.md)] omfatter et element for faktabokskontroll på en rekke viktige listesider som gir ytterligere innsikt i dataene i listen. Når du flytter mellom radene i listen, er oppdateres og filtreres rapporten for den valgte posten. Du kan opprette egendefinerte rapporter som skal vises i denne kontrollen. Det finnes imidlertid noen få regler du må følge, for å sikre at rapporter fungerer som forventet.  

## <a name="prerequisites"></a>Forutsetninger

- En Power BI-konto.
- Power BI Desktop.

Hvis du vil ha mer informasjon om hvordan du kommer i gang, kan du se [Bruke [!INCLUDE[prod_short](includes/prod_short.md)] som en datakilde for Power BI](across-how-use-financials-data-source-powerbi.md).

## <a name="defining-the-report-data-set"></a>Definere rapportdatasettet

Angi datakilden som inneholder dataene som er knyttet til listen. Hvis du for eksempel vil opprette en rapport for Salgsoversikt, sikrer du at datasettet inneholder informasjon knyttet til salg.  

## <a name="defining-the-report-filter"></a>Definere rapportfilteret

For å oppdatere dataene til den valgte posten i listen legger du til et filter i rapporten. Filteret må inneholde et felt for datakilden som brukes som *primærnøkkelen*. I de fleste tilfeller er primærnøkkelen for en liste **Nr.** -feltet.

Hvis du vil definere et filter for rapporten, velger du primærnøkkelen fra listen over tilgjengelige felt, og deretter dra og slippe feltet i **Rapportfilter**-delen. Filteret må være et grunnleggende rapportfilter som er definert for alle sider. Det kan ikke være en side, en visualisering eller et avansert filter.

![Angi rapportfilteret for Salgsfaktura-aktivitetsrapporten](./media/across-how-use-powerbi-reports-factbox/financials-powerbi-report-filter-v3.png)

## <a name="setting-the-report-size-and-color"></a>Angi rapportstørrelsen og -fargen

Størrelsen på rapporten må settes til 325 x 310 piksler. Denne størrelsen gir riktig skalering av rapporten på den ledige plassen for Power BI-faktabokskontrollen i [!INCLUDE[prod_short](includes/prod_short.md)]. Hvis du vil definere størrelsen på rapporten, fokusere utenfor oppsettsområdet til rapporten, og velg deretter malerrulleikonet.

![Angi bredden og høyden på Salgsfaktura-aktivitetsrapporten](./media/across-how-use-powerbi-reports-factbox/financials-powerbi-report-sizing-v3.png)

Du kan endre bredden og høyden på rapporten ved å velge **Egendefinert** i **Type**-feltet.

Hvis du vil at bakgrunnen i rapporten skal blandes med bakgrunnsfargen til Power BI-faktabokskontrollen, setter du rapportbakgrunnsfargen til *#FFFFFF*. 

## <a name="using-reports-with-multiple-pages"></a>Bruke rapporter med flere sider

Du kan opprette én enkelt rapport med flere sider med Power BI. Når det gjelder rapporter som skal vises på listesider, anbefaler vi ikke at de har flere enn én side. Power BI-faktaboksen viser bare den første siden i rapporten.

## <a name="naming-the-report"></a>Gi navn til rapporten

Gi rapporten et navn som inneholder navnet på listesiden som er knyttet til rapporten. Hvis rapporten for eksempel er for listesiden **Leverandør**, tar du med ordet *leverandør* et sted i navnet.  

Denne navnekonvensjonen er ikke et krav. Den gjør det imidlertid raskere å velge rapporter i [!INCLUDE[prod_short](includes/prod_short.md)]. Når siden for valg av rapport åpnes fra en listeside, filtreres den automatisk basert på sidenavnet. Denne filtreringen utføres for å begrense antall rapporter som vises. Brukere kan fjerne filteret for å få en fullstendig liste over rapporter som er tilgjengelige i Power BI.  

## <a name="fixing-problems"></a>Løse problemer

Denne delen inneholder en løsning for de vanligste problemene som kan oppstå når du oppretter en Power BI-rapport.  

#### <a name="you-cant-see-a-report-on-the-select-report-page"></a>Det er en rapport som ikke vises på Velg rapport-siden

Dette skjer sannsynligvis fordi navnet på rapporten ikke inneholder navnet på listesiden. Fjern filteret for å få en fullstendig liste over tilgjengelige Power BI-rapporter.  

#### <a name="report-is-loaded-but-blank-not-filtered-or-filtered-incorrectly"></a>Rapporten er lastet inn, men tom, ikke filtrert eller filtrert feil

Kontroller at rapportfilteret inneholder riktig primærnøkkel. I de fleste tilfeller er dette **Nr.**-feltet, men i **Finanspost**-tabellen, for eksempel, må du bruke **Løpenr.**-feltet.

#### <a name="report-is-loaded-but-it-shows-a-page-you-didnt-expect"></a>Rapporten er lastet inn, men den viser en side du ikke forventet

Kontroller at siden du vil vise, er den første siden i rapporten.  

#### <a name="report-appears-with-an-unwanted-gray-boarder-or-its-too-small-or-too-large"></a>Rapporten vises med en uønsket grå kantlinje, eller den er for liten eller for stor

Kontroller at størrelsen på rapporten er satt til 325 x 310 piksler. Lagre rapporten, og deretter oppdater listesiden.  

## <a name="see-related-training-at-microsoft-learn"></a>Se relatert opplæring på [Microsoft Learn](/learn/modules/configure-powerbi-excel-dynamics-365-business-central/index)

## <a name="see-also"></a>Se også

[Aktivere forretningsdata for Power BI](admin-powerbi.md)  
[Bruke [!INCLUDE[prod_short](includes/prod_short.md)] som en Power BI-datakilde](across-how-use-financials-data-source-powerbi.md)  
[Komme i gang](product-get-started.md)  
[Konfigurere [!INCLUDE[prod_short](includes/prod_short.md)]](setup.md)  
[Finans](finance.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]