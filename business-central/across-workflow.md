---
title: Arbeidsflyter i dynamisk 365 Business Central
description: Bruk arbeidsflyter til å koble forretningsprosessoppgaver som utføres av forskjellige brukere. Systemoppgaver, for eksempel automatisk bokføring, kan tas med som arbeidsflyttrinn.
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 06/11/2021
ms.author: edupont
ms.openlocfilehash: 02f03c3b3423de2b78aea7f4e61c65c968290341
ms.sourcegitcommit: ef80c461713fff1a75998766e7a4ed3a7c6121d0
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 02/15/2022
ms.locfileid: "8130882"
---
# <a name="workflows-in-dynamics-365-business-central"></a>Arbeidsflyter i Dynamics 365 Business Central

Du kan definere og bruke arbeidsflyter som kobler forretningsprosessoppgaver som utføres av forskjellige brukere. Systemoppgaver, for eksempel automatisk bokføring, kan tas med som trinn i arbeidsflyter, før eller etterfulgt av brukeroppgaver. Å be om og gi godkjenning til å opprette nye oppføringer er typiske arbeidsflyttrinn.  

 På **Arbeidsflyt**-siden oppretter du en arbeidsflyt ved å føre opp de involverte trinnene på linjene. Hvert trinn består av en arbeidsflythendelse, endret av hendelsesbetingelsene, og et arbeidsflytsvar, endret av svaralternativer. Du definerer arbeidsflyttrinn ved å fylle ut felt på arbeidsflytlinjer fra faste lister over verdier for hendelse og svar som representerer scenarier som støttes av programkoden.  

 Standardversjonen av [!INCLUDE[prod_short](includes/prod_short.md)] omfatter en rekke forhåndskonfigurerte arbeidsflyter representert av arbeidsflytmaler som du kan kopiere for å opprette arbeidsflyter. Koden for arbeidsflytmaler som er lagt inn av Microsoft, har prefikset "MS-". Hvis du vil ha mer informasjon, kan du se listen over arbeidsflytmaler på siden Arbeidsflytmaler.  

 Hvis et forretningsscenario krever en arbeidsflythendelse eller et arbeidsflytsvar som ikke støttes, kan du bruke Power Automate eller samarbeide med en Microsoft-partner for å tilpasse programkoden. Hvis du vil ha mer informasjon, kan du se [Bruke [!INCLUDE[prod_short](includes/prod_short.md)] i en automatisk arbeidsflyt](across-how-use-financials-data-source-flow.md).

Alle arbeidsflytmaler du oppretter med Power Automate, legges til i listen over arbeidsflytmaler i [!INCLUDE[prod_short](includes/prod_short.md)]. Hvis du vil ha mer informasjon, se [Bruke Business Central i en automatisk arbeidsflyt](across-how-use-financials-data-source-flow.md).  

 Tabellen nedenfor beskriver en sekvens av oppgaver, og har koblinger til emnene som beskriver dem.  

|**Hvis du vil**|**Se**|  
|------------|-------------|  
|Definer arbeidsflytbrukere, angi hvordan brukere skal varsles, og opprett nye arbeidsflyter. For nye arbeidsflyter for scenarier som ikke støttes, kan du implementere nødvendige arbeidsflytelementer ved å tilpasse programkoden.|[Konfigurere arbeidsflyter](across-set-up-workflows.md)|  
|Aktiver arbeidsflyter, handle på arbeidsflytvarsler, inkludert forespørselsgodkjenninger, og godkjenn forespørsler om å utføre et arbeidsflyttrinn. Arkiver og slett arbeidsflyter.|[Bruke arbeidsflyter](across-use-workflows.md)|  

## <a name="see-also"></a>Se også

[Salg](sales-manage-sales.md)  
[Innkjøp](purchasing-manage-purchasing.md)  
[Administrere prosjekter](projects-manage-projects.md)  
[Arbeide med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]