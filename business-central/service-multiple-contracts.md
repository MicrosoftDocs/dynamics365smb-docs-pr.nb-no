---
title: Flere kontrakter | Microsoft-dokumentasjon
description: Avhengig av servicenivåavtalene du har med kunden, må du kanskje behandle en servicevare på flere enn én servicekontrakt.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: c6410f1b96aa1c1f8251738184db07aba0d94c4b
ms.sourcegitcommit: ddbb5cede750df1baba4b3eab8fbed6744b5b9d6
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 10/01/2020
ms.locfileid: "3915288"
---
# <a name="multiple-contracts"></a>Flere kontrakter
Avhengig av servicenivåavtalene du har med kunden, må du kanskje behandle en servicevare på flere enn én servicekontrakt.  
  
Ved å behandle en servicevare for flere kontrakter, kan du gjøre følgende:  
  
* Utstede forskjellige kontrakter for samme servicevare.  
* Foreta service på deler separat.  
* Vurder forskjellig kompetanse som kreves for å foreta service på forskjellige deler av en servicevare, for eksempel mekaniske komponenter og programvare.  
* Angi forskjellige responstider og -frekvenser for service på forskjellige deler av servicevaren.  
* Gå i gang med forskjellige aktiviteter som må utføres på en servicevare, når servicevaren krever forskjellige typer service, til forskjellige tidspunkt.  
* Velg og tilordne et riktig kontraktnummer til en servicevarelinje når du oppretter en serviceordre.  
* Behandle relevant finansiell informasjon om servicevarer og servicenivåavtaler.  
  
Vurder følgende eksempler for bruk av flerkontraktsfunksjonalitet:  
  
## <a name="creating-multiple-contracts-per-service-item"></a>Opprette flere kontrakter per servicevare  
Du kan opprette en servicekontrakt eller et kontrakttilbud manuelt for servicevarer som allerede er registrert i ikke-avbrutte kontrakter som tilhører av samme kunde. Følg vanlig fremgangsmåte for opprettelse av servicekontrakter og servicekontrakttilbud når du skal gjøre dette. Hvis du vil ha mer informasjon, kan du se [Arbeide med servicekontrakter og servicekontrakttilbud](service-how-to-create-service-contracts-and-service-contract-quotes.md).  
  
Når du legger til en servicevare på en kontraktlinje som er registrert i andre servicekontrakter eller kontrakttilbud, vises en advarsel som sier at servicevaren allerede tilhører én eller flere servicekontrakter eller kontrakttilbud. Hvis du bekrefter denne meldingen, kopieres alle aktuelle servicevareopplysninger til en nyopprettet kontraktlinje.  
  
## <a name="copying-documents"></a>Kopiere dokumenter  
Du kan automatisk opprette en servicekontrakt eller et kontrakttilbud for servicevarer som allerede er registrert i andre servicekontrakter eller kontrakttilbud, ved å bruke handlingen **Kopier fra dokument**.  
  
## <a name="creating-service-orders-for-multiple-contracts"></a>Opprette serviceordrer for flere kontrakter  
Du kan manuelt opprette en serviceordre for en servicevare som er registrert i flere aktive kontrakter. En servicekontrakt er aktiv hvis den er undertegnet og ikke er utgått.  
  
## <a name="see-also"></a>Se også  
[Oppfylle servicekontrakter](service-fulfill-service-contracts.md)  
[Opprette serviceordrer](service-how-to-create-service-orders.md)  
