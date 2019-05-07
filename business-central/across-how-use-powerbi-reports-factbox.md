---
title: Vise egendefinerte Power BI-rapporter | Microsoft Docs
description: Du kan bruke Power BI-rapporter til å få ytterligere innsikt i data i lister.
services: project-madeira
documentationcenter: ''
author: edupont04
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: business intelligence, KPI, Odata, Power App, SOAP, analysis
ms.date: 04/01/2019
ms.author: edupont
ms.openlocfilehash: 29c7b7656632d2103a16025848a6ddc82650353e
ms.sourcegitcommit: bd78a5d990c9e83174da1409076c22df8b35eafd
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 03/31/2019
ms.locfileid: "937897"
---
# <a name="viewing-list-data-in-power-bi-reports-in-business-central"></a>Vise listedata i Power BI-rapporter i Business Central 
[!INCLUDE[d365fin](includes/d365fin_md.md)] inkluderer en faktaboks kontrollelement på en rekke viktige listesider som gir ytterligere innsikt i dataene i listen. Når du flytter mellom radene i listen, er oppdateres og filtreres rapporten for den valgte posten. Du kan opprette egendefinerte rapporter for å vises i kontrollen, men det finnes et par regler å følge når du oppretter rapporter for å sikre at de gir den ønskede virkemåten.  

> [!NOTE]  
>   Du må ha en gyldig konto med [!INCLUDE[d365fin](includes/d365fin_md.md)] og med Power BI. Du må også laste ned [Power BI Desktop](https://powerbi.microsoft.com/en-us/desktop/). Hvis du vil ha mer informasjon, kan du se [Bruke [!INCLUDE[d365fin](includes/d365fin_md.md)] som en datakilde for Power BI](across-how-use-financials-data-source-powerbi.md).  

## <a name="report-data-set"></a>Rapportdatasett
Når du oppretter rapporten i Power BI Desktop, kan du angi datakilden eller webtjenesten som inneholder dataene som er knyttet til listen som du vil knytte til rapporten. For eksempel, hvis du vil opprette en rapport for salgslisten, sikre at datasettet ikke inneholder informasjon som er knyttet til salg.  

Hvis du vil filtrere data i rapporter som er basert på posten som er valgt på listesiden, må den primære nøkkelen brukes som et rapportfilter. Primærnøklene må være en del av datasettet for at rapportene skal filtreres på riktig måte. I de fleste tilfeller er primærnøkkelen for en liste **Nr.** -feltet.  

## <a name="defining-the-report-filter"></a>Definere rapportfilteret
Rapporten må ha et grunnleggende rapportfilter (ikke en side eller et visuelt filter og ikke et avansert filter) for å filtreres på riktig måte i Power BI-faktaboksen for kontrollen. Filteret som blir sendt til Power BI-rapporten fra hver listeside baseres på primærnøkkelen som beskrevet i forrige del.  

Hvis du vil definere et filter for rapporten, velger du primærnøkkelen fra listen over tilgjengelige felt, og deretter dra og slippe feltet i **Rapportfilter**-delen.  

![Angi rapportfilteret for Salgsfaktura-aktivitetsrapporten](./media/across-how-use-powerbi-reports-factbox/financials-powerbi-report-filter.png)

## <a name="report-size-and-color"></a>Rapportstørrelse og -farge
Størrelsen på rapporten må settes til 325 x 310 piksler. Dette er nødvendig for riktig skalering av rapporten i den tilgjengelige plassen som er tillatt av Power BI-faktabokskontrollen. Hvis du vil definere størrelsen på rapporten, fokusere utenfor oppsettsområdet til rapporten, og velg deretter malerrulleikonet.

![Angi bredden og høyden på Salgsfaktura-aktivitetsrapporten](./media/across-how-use-powerbi-reports-factbox/financials-powerbi-report-sizing.png)

Du kan endre bredden og høyden på rapporten ved å velge **Egendefinert** i **Type**-feltet.

På samme måte, hvis du vil få bakgrunnen på rapporten til å blandes inn i bakgrunnsfargen for Power BI-faktabokskontrollen, defineres den egendefinerte rapportbakgrunnsfargen *E5E5E5*. Dette er valgfritt.  

## <a name="reports-with-multiple-pages"></a>Rapporter med flere sider
Du kan opprette én enkelt rapport med flere sider med Power BI. Bilder som du vil se på [!INCLUDE[d365fin](includes/d365fin_md.md)]-listesider, må være på den første siden i rapporten i Power BI.  

> [!NOTE]  
>  Faktaboksen Power BI kan bare vise den første siden i rapporten. Hvis du vil vise andre sider, må du utvide rapporten og bruke fanene nederst i rapporten til å navigere til andre sider.  

## <a name="saving-your-report"></a>Lagre rapporten

Når du lagrer rapporten, er det en anbefalt fremgangsmåte at navnet på rapporten inneholder navnet på listesiden du vil vise i rapporten. For eksempel må ordet *Leverandør* ligge et sted i rapportnavnet for rapporter som du vil gjøre tilgjengelig i leverandøroversikten.  

Dette er ikke et krav. Det vil imidlertid gjøre prosessen med å velge rapporter raskere. Når rapportsiden åpnes fra en listeside, vil vi sende et filter basert på navnet på siden for å avgrense rapporter som vises.  Du kan fjerne filteret for å få en fullstendig liste over rapporter som er tilgjengelige for deg i Power BI.  

## <a name="troubleshooting"></a>Feilsøking
Denne delen inneholder en løsning for de vanligste problemene som kan oppstå når du oppretter en Power BI-rapport.  

**Brukeren ser ikke en rapport på siden Velg rapport de vil velge** Hvis du ikke kan velge en rapport, en mulig løsning er å bekrefte navnet på rapporten for å sikre at den inneholder navnet på siden. Du kan fjerne filteret for å få en fullstendig liste over rapporter som er tilgjengelige i Power BI.  

**Rapporten er lastet inn, men tom, ikke filtrert eller filtrert feil** Kontroller at rapportfilteret inneholder den høyre primærnøkkelen. I de fleste tilfeller er det **Nr.**- feltet, men i **Finanspost**-tabellen, for eksempel, må du bruke **Løpenr.**-feltet.

**Rapporten er lastet inn, men det viser siden du ikke har forventet** Kontroller at siden du vil vise er den første siden i rapporten.  

**Rapporten vises med uønsket grå kantlinjer, er for liten eller for stor**

Kontroller at størrelsen på rapporten er satt til 325 x 310 piksler. Lagre rapporten, og deretter oppdater listesiden.  

## <a name="see-also"></a>Se også
[Bruke [!INCLUDE[d365fin](includes/d365fin_md.md)] som en Power BI-datakilde](across-how-use-financials-data-source-powerbi.md)  
[Komme i gang](product-get-started.md)    
[Konfigurere [!INCLUDE[d365fin](includes/d365fin_md.md)]](setup.md)    
[Finans](finance.md)  
