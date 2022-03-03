---
title: Definere selskapskonfigurasjon
description: Som partner kan du få Business Central konfigurert riktig til kunden med standardkonfigurasjoner eller kundespesifikke konfigurasjoner som du gjør i konfigurasjonspakker.
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/01/2021
ms.author: edupont
ms.openlocfilehash: 841d57ec0e5897ee0395e498ed24dc19b4fcbaea
ms.sourcegitcommit: ef80c461713fff1a75998766e7a4ed3a7c6121d0
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 02/15/2022
ms.locfileid: "8143937"
---
# <a name="set-up-company-configuration"></a>Definere selskapskonfigurasjon
Implementeringsprosessen begynner med Microsoft-partneren. Som en partneren er du ansvarlig for å tenke gjennom konfigurasjonsdetaljer og lage en pakke som kunden enkelt kan bruke. Før du oppretter et nytt selskap i [!INCLUDE [prod_short](includes/prod_short.md)] lokalt, bør du planlegge hvordan det skal konfigureres. Du må vurdere grunnleggende oppsettsdata og hvilke typer data [!INCLUDE[prod_short](includes/prod_short.md)]-løsningen vil kreve. Du grupperer all denne informasjonen i konfigurasjonspakker.

RapidStart Services gir deg også verktøy som du vil bruke til å overføre eldre data, for eksempel kunder og leverandører.  

Vi anbefaler at du oppretter konfigurasjonspakker der de fleste av oppsettstabellene allerede er utfylt, slik at kunder bare trenger å ende noen få innstillinger etter at pakken tas i bruk. Når du for eksempel oppretter et nytt selskap, blir tabellene **Nummerserie** og **Nr.serielinje** fylt ut med et sett med nummerserier og startnumre. Den tilsvarende **Nr. serie**-feltet i oppsettstabellene er fylles også ut automatisk. Du trenger ikke å utføre oppgaver som å angi nummerserier og andre grunnleggende oppsettsdata. Du kan også manuelt endre alle standarddata som brukes sammen med RapidStart Services, ved hjelp av konfigurasjonsforslaget.  

Konfigurasjonspakkene bygger på et forhåndskonfigurert selskap. Når du har definert et selskap som oppfyller dine behov, kan du opprette en konfigurasjonspakke som inneholder relevante data fra dette selskapet. Deretter kan du bruke den når du oppretter et nytt selskap som skal konfigureres på samme måte.  

For å forenkle import av hoveddata, for eksempel kunde- og leverandørinformasjon, kan du bruke konfigurasjonsmaler. Konfigurasjonsmaler inneholder et sett med standardinnstillinger, som tilordnes automatisk til postene som importeres til [!INCLUDE[prod_short](includes/prod_short.md)].

Tabellen nedenfor beskriver en sekvens av oppgaver, og har koblinger til emner som beskriver dem.

|**Hvis du vil**|**Se**|  
|------------|-------------|  
|Planlegge en selskapskonfigurasjon ved å fylle ut konfigurasjonsforslaget.|[Behandle selskapskonfigurasjon i et forslag](admin-how-to-manage-company-configuration-in-a-worksheet.md)|  
|Opprett en konfigurasjonspakke, tilpass en pakke, tilordne tabeller til en pakke, se gjennom eller rediger eksisterende kundedata, opprette det nye selskapet og flytt deretter testdata til produksjonsmiljøet.|[Klargjøre en konfigurasjonspakke](admin-how-to-prepare-a-configuration-package.md)|

Du kan også opprette konfigurasjonspakker med standardkonfigurasjoner som du kan bruke igjen og igjen. Hvis du vil ha mer informasjon, kan du se [Konfigurer standard firmakonfigurasjonspakker](/dynamics365/business-central/dev-itpro/administration/set-up-standard-company-configuration-packages) i utvikler- og administrasjonsinnholdet.  

## <a name="see-also"></a>Se også

[Konfigurere et selskap med RapidStart Services](admin-set-up-a-company-with-rapidstart.md)  
[Administrasjon](admin-setup-and-administration.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]