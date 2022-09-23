---
title: Arbeidsflyter i dynamisk 365 Business Central
description: Bruk de innebygde funksjonene i arbeidsflyten til å definere godkjenningsarbeidsflyter til å supplere automatiserte arbeidsflyter basert på Power Automate. Du kan konfigurere trinn for å tildele oppgaver til forskjellige personer som en del av de ulike forretningsprosessoppgavene.
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 05/12/2022
ms.author: edupont
ms.openlocfilehash: 0bd4c54bc089906877052efdbf471fc3dbe1fc30
ms.sourcegitcommit: 3acadf94fa34ca57fc137cb2296e644fbabc1a60
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 09/19/2022
ms.locfileid: "9533433"
---
# <a name="workflows-in-dynamics-365-business-central"></a>Arbeidsflyter i Dynamics 365 Business Central

Du kan definere og bruke arbeidsflyter som kobler forretningsprosessoppgaver som utføres av forskjellige brukere. Systemoppgaver, for eksempel automatisk bokføring, kan tas med som trinn i arbeidsflyter, før eller etterfulgt av brukeroppgaver. Å be om og gi godkjenning til å opprette nye oppføringer er typiske arbeidsflyttrinn.  

Standardversjonen av [!INCLUDE [prod_short](includes/prod_short.md)] støtter tre typer arbeidsflyter:

* Automatisert godkjenningsarbeidsflyt basert på innebygde arbeidsflytmaler  

  På siden **Arbeidsflytmaler** kan du se alle tilgjengelige arbeidsflyter. Prøveversjonen av [!INCLUDE[prod_short](includes/prod_short.md)] omfatter mange forhåndskonfigurerte arbeidsflyter representert av arbeidsflytmaler som du kan kopiere for å opprette arbeidsflyter. Når du åpner en arbeidsflytmal fra siden **Arbeidsflytmaler**, og arbeidsflytens navn starter med *MS-*, legges arbeidsflytmalen til av Microsoft.  
* Automatiserte flyter du konfigurerer selv  

  Alle arbeidsflytmaler du oppretter med Power Automate, legges til i listen over arbeidsflytmaler i [!INCLUDE[prod_short](includes/prod_short.md)]. Hvis du vil ha mer informasjon, kan du se [Bruk Business Central i Power Automate-flyter](across-how-use-financials-data-source-flow.md).  
* Manuelt utløste flyter fra handlingen **Automatiser** (bare [!INCLUDE [prod_short](includes/prod_short.md)] på nettet). Hvis du vil ha mer informasjon, kan du se [Manuelle direkteflyter](across-how-use-financials-data-source-flow.md#manual-instant-flows).  

## <a name="power-automate-flows"></a>Power Automate-flyter

Ved å bruke [!INCLUDE [prod_short](includes/prod_short.md)] på nettet kan du registrere deg for Power Automate og deretter bygge kraftige automatiserte flyter som du kan kjøre fra [!INCLUDE [prod_short](includes/prod_short.md)]. Hvis du vil ha mer informasjon, kan du se [Bruk [!INCLUDE[prod_short](includes/prod_short.md)] i Power Automate-flyter](across-how-use-financials-data-source-flow.md).  

## <a name="automated-approval-workflows"></a>Automatiserte godkjenningsarbeidsflyter

Du kan opprette en godkjenningsarbeidsflyt ved å føre opp de involverte trinnene på linjene. Hvert trinn består av en arbeidsflythendelse, endret av hendelsesbetingelsene, og et arbeidsflytsvar, endret av svaralternativer. Du definerer arbeidsflyttrinn ved å fylle ut felt på arbeidsflytlinjer fra faste lister over verdier for hendelse og svar som representerer scenarier som støttes av programkoden.  

[!INCLUDE[workflow](includes/workflow.md)]

Se følgende artikler for å konfigurere og bruke arbeidsflyter som ikke er definert, i Power Automate:  

|**Hvis du vil**|**Se**|  
|------------|-------------|  
|Definer arbeidsflytbrukere, angi hvordan brukere skal varsles, og opprett nye arbeidsflyter. For nye arbeidsflyter for scenarier som ikke støttes, kan du implementere nødvendige arbeidsflytelementer ved å tilpasse programkoden.|[Konfigurere arbeidsflyter](across-set-up-workflows.md)|  
|Aktiver arbeidsflyter, handle på arbeidsflytvarsler, inkludert forespørselsgodkjenninger, og godkjenn forespørsler om å utføre et arbeidsflyttrinn. Arkiver og slett arbeidsflyter.|[Bruke arbeidsflyter](across-use-workflows.md)|  

## <a name="see-related-microsoft-training"></a>Se relatert [Microsoft-opplæring](/training/modules/create-workflows/)

## <a name="see-also"></a>Se også

[Salg](sales-manage-sales.md)  
[Innkjøp](purchasing-manage-purchasing.md)  
[Administrere prosjekter](projects-manage-projects.md)  
[Arbeid med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  
[Bruk [!INCLUDE[prod_short](includes/prod_short.md)] i Power Automate-flyter](across-how-use-financials-data-source-flow.md)  
[Feilsøk automatiserte arbeidsflyter for [!INCLUDE[prod_short](includes/prod_short.md)]](across-flow-troubleshoot.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
