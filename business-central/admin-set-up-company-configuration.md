---
title: Definere selskapskonfigurasjon | Microsoft-dokumentasjon
description: Implementeringsprosessen starter med Business Central-løsningen som kreves. Du grupperer all denne informasjonen i konfigurasjonspakker.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/01/2021
ms.author: edupont
ms.openlocfilehash: 3eefa0fcb40b4e925ca653f223f2d97ed10f370e
ms.sourcegitcommit: 766e2840fd16efb901d211d7fa64d96766ac99d9
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 03/31/2021
ms.locfileid: "5777244"
---
# <a name="set-up-company-configuration"></a>Definere selskapskonfigurasjon
Implementeringsprosessen begynner med Microsoft-partneren. Partneren er ansvarlig for å tenke gjennom konfigurasjonsdetaljer og lage en pakke som kunden enkelt kan bruke. Før du oppretter et nytt selskap, bør du planlegge hvordan det skal konfigureres. Du må vurdere grunnleggende oppsettsdata og hvilke typer data [!INCLUDE[prod_short](includes/prod_short.md)]-løsningen vil kreve. Du grupperer all denne informasjonen i konfigurasjonspakker.

RapidStart Services gir deg også verktøy som du vil bruke til å overføre dine eldre data, for eksempel kunder og leverandører.  

Vi anbefaler at du oppretter konfigurasjonspakker der de fleste av oppsettstabellene allerede er utfylt, slik at kunder bare trenger å ende noen få innstillinger etter at pakken tas i bruk. Når du for eksempel oppretter et nytt selskap, blir tabellene **Nummerserie** og **Nr.serielinje** fylt ut med et sett med nummerserier og startnumre. Den tilsvarende **Nr. serie**-feltet i oppsettstabellene er fylles også ut automatisk. Du trenger ikke å utføre oppgaver som å angi nummerserier og andre grunnleggende oppsettsdata. Du kan også manuelt endre alle standarddata som brukes sammen med RapidStart Services, ved hjelp av konfigurasjonsforslaget.  

Konfigurasjonspakkene bygger på et forhåndskonfigurert selskap. Når du har definert et selskap som oppfyller dine behov, kan du opprette en konfigurasjonspakke som inneholder relevante data fra dette selskapet. Deretter kan du bruke den når du oppretter et nytt selskap som skal konfigureres på samme måte.  

For å forenkle import av hoveddata, for eksempel kunde- og leverandørinformasjon, kan du bruke konfigurasjonsmaler. Konfigurasjonsmaler inneholder et sett med standardinnstillinger, som tilordnes automatisk til postene som importeres til [!INCLUDE[prod_short](includes/prod_short.md)].

Tabellen nedenfor beskriver en sekvens av oppgaver, og har koblinger til emner som beskriver dem.

|**Hvis du vil**|**Se**|  
|------------|-------------|  
|Planlegge en selskapskonfigurasjon ved å fylle ut konfigurasjonsforslaget.|[Behandle selskapskonfigurasjon i et forslag](admin-how-to-manage-company-configuration-in-a-worksheet.md)|  
|Opprett en konfigurasjonspakke, tilpass en pakke, tilordne tabeller til en pakke, se gjennom eller rediger eksisterende kundedata, opprette det nye selskapet og flytt deretter testdata til produksjonsmiljøet.|[Klargjøre en konfigurasjonspakke](admin-how-to-prepare-a-configuration-package.md)| 

## <a name="see-also"></a>Se også  
[Konfigurere et selskap med RapidStart Services](admin-set-up-a-company-with-rapidstart.md)  
[Administrasjon](admin-setup-and-administration.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]