---
title: Arbeidsflyter i Dynamics 365 Business Central
description: Bruk innebygde funksjoner i arbeidsflyten til å definere godkjenningsarbeidsflyter til å supplere automatiserte arbeidsflyter basert på Power Automate. Du kan konfigurere trinn for å tildele oppgaver til forskjellige personer som en del av de ulike forretningsprosessoppgavene.
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 09/13/2022
ms.author: edupont
ms.openlocfilehash: ecaaf9bbb56e1c1b47f9f617319b32f32a2920fd
ms.sourcegitcommit: 9049f75c86dea374e5bfe297304caa32f579f6e4
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 09/23/2022
ms.locfileid: "9585625"
---
# <a name="workflows-in-dynamics-365-business-central"></a>Arbeidsflyter i Dynamics 365 Business Central

Du kan definere og bruke arbeidsflyter til å koble forretningsprosessoppgaver som utføres av forskjellige brukere. Systemoppgaver, for eksempel automatisk bokføring, kan tas med som trinn i arbeidsflyter, før eller etterfulgt av brukeroppgaver. Å be om og gi godkjenning til å opprette nye oppføringer er typiske arbeidsflyttrinn.

Standardversjonen av [!INCLUDE [prod_short](includes/prod_short.md)] støtter tre typer arbeidsflyter:

* Godkjenningsarbeidsflyt basert på innebygde arbeidsflytmaler

  På siden **Arbeidsflytmaler** kan du se alle tilgjengelige arbeidsflyter. Prøveversjonen av [!INCLUDE[prod_short](includes/prod_short.md)] omfatter mange forhåndskonfigurerte arbeidsflyter representert av arbeidsflytmaler som du kan kopiere for å opprette nye. Når du åpner en mal fra siden **Arbeidsflytmaler** og arbeidsflytnavnet starter med *MS-*, ble malen lagt til av Microsoft.
  
* Power Automate-flyter du konfigurerer selv

  Alle arbeidsflytmaler du oppretter med Microsoft Power Automate, legges til i listen over arbeidsflytmaler i [!INCLUDE[prod_short](includes/prod_short.md)]. Finn ut mer under [Bruk [!INCLUDE[prod_short](includes/prod_short.md)] i Power Automate-flyter](across-how-use-financials-data-source-flow.md). 
  
* Direkteflyter manuelt utløst av handlingen **Automatiser** (bare [!INCLUDE [prod_short](includes/prod_short.md)] på nettet).

  Opprett og manuelt utløs en Power Automate-flyt i en [!INCLUDE[prod_short](includes/prod_short.md)]-post, for eksempel en kunde, vare eller ordre, med alternativer for å manipulere informasjon både internt og eksternt (ved hjelp av integrerte verktøy). Finn ut mer i delen [Direkteflyter](across-how-use-financials-data-source-flow.md#instant-flows).

## <a name="power-automate-flows"></a>Power Automate-flyter

Ved hjelp av [!INCLUDE [prod_short](includes/prod_short.md)] online kan du registrere deg for Power Automate for å bygge kraftige automatiserte arbeidsflyter. Du kan kjøre arbeidsflytene i [!INCLUDE [prod_short](includes/prod_short.md)], koble sammen interne og eksterne datakilder med data og verktøy, uten å kodekunnskap.

Power Automate-flyter kan utløses av hendelser (for eksempel oppretting, endring eller sletting av poster eller dokumenter), og de kan kjøres i en brukerdefinert tidsplan eller ved behov (kjent som en **direkteflyt**).

## <a name="approval-workflows"></a>Arbeidsflyter for godkjenning

Du kan opprette en godkjenningsarbeidsflyt ved å føre opp de involverte trinnene på linjene. Hvert trinn består av en arbeidsflythendelse, endret av hendelsesbetingelsene, og et arbeidsflytsvar, endret av svaralternativer. Du definerer arbeidsflyttrinn ved å fylle ut felter på arbeidsflytlinjer ved å bruke faste lister over verdier for hendelse og svar som representerer scenarioer som støttes av programkoden.<!--What are the "values"? Can we give an example?-->

Eksempler på hendelser for arbeidsflyter for godkjenning omfatter blant annet oppretting av ordrer eller bestillinger / tilbud / fakturaer, prisendringer og leverandør- eller kundeendringer.

[!INCLUDE[workflow](includes/workflow.md)]

| **Hvis du vil** | **Se** |
|--|--|
| Definer brukere for arbeidsflyt for godkjenning, angi hvordan brukere skal varsles, og opprett nye arbeidsflyter. (For å opprette nye arbeidsflyter for scenarier som ikke støttes, kan du implementere nødvendige arbeidsflytelementer ved å tilpasse programkoden.) | [Konfigurer godkjenningsarbeidsflyter](across-set-up-workflows.md) |
| Aktiver arbeidsflyter for godkjenning, handle på arbeidsflytvarsler, inkludert å be om og godkjenne et flyttrinn. Arkiver og slett arbeidsflyter. | [Bruk godkjenningsarbeidsflyter](across-use-workflows.md) |
| Integrer selskapsdata med Power Automate-arbeidsflyter ved hjelp av både interne og eksterne kilder og hendelser for å opprette og automatisere oppgaver eller arbeidsflyter. | [Bruk Power Automate-flyter i [!INCLUDE[prod_short](includes/prod_short.md)]](across-how-use-financials-data-source-flow.md) |

## <a name="see-related-microsoft-training"></a>Se relatert [Microsoft-opplæring](/training/modules/create-workflows/)

## <a name="see-also"></a>Se også

[Salg](sales-manage-sales.md)  
[Innkjøp](purchasing-manage-purchasing.md)  
[Administrere prosjekter](projects-manage-projects.md)  
[Arbeid med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  
[Feilsøk automatiserte arbeidsflyter for [!INCLUDE[prod_short](includes/prod_short.md)]](across-flow-troubleshoot.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
