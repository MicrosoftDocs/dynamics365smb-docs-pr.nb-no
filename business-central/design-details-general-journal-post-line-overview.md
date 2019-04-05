---
title: Oversikt over Finanskladd – bokfør linje | Microsoft-dokumentasjon
description: Dette emnet introduserer endringer i Kodeenhet 12, **Finanskladd – bokfør linje**, som er det store programobjektet for finansbokføring og det eneste stedet å sette inn finansposter, mva-poster og kunde- og leverandørposter.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: design, general ledger, post
ms.date: 10/01/2018
ms.author: sgroespe
ms.openlocfilehash: db90633823f12650f796735a9a83bec8edb60cb9
ms.sourcegitcommit: 1bcfaa99ea302e6b84b8361ca02730b135557fc1
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 03/08/2019
ms.locfileid: "802448"
---
# <a name="general-journal-post-line-overview"></a>Oversikt over Finanskladd – bokfør linje
Kodeenhet 12, **Finanskladd – bokfør linje**, er det store programobjektet for finansbokføring og det eneste stedet å sette inn finansposter, mva-poster og kunde- og leverandørposter. Denne kodeenheten brukes også for alle operasjoner med Utlign, Opphev utligning og Tilbakefør.  
  
Selv om kodeenheten har blitt forbedret i hver utgivelse over de siste ti årene, har arkitekturen i hovedsak vært den samme. Kodeenheten ble svært stor, med omtrent 7 600 kodelinjer. I denne utgivelsen av [!INCLUDE[d365fin](includes/d365fin_md.md)] er arkitekturen endret, og kodeenheten er forenklet og gjort enklere å vedlikeholde. Denne dokumentasjonen beskriver endringene og inneholder informasjon du trenger for å oppgradere.  
  
## <a name="old-architecture"></a>Gammel arkitektur  
Den gamle arkitekturen hadde følgende funksjoner:  
  
* Det var omfattende bruk av globale variabler, som øker risikoen for skjulte feil som skyldes bruk av variabler med feil omfang.  
* Det var mange lange prosedyrer (med flere enn 100 kodelinjer) som også hadde høy syklomatisk kompleksitet (det vil si mange nestede CASE-, REPEAT- og IF-setninger), som gjorde det veldig vanskelig å lese og vedlikeholde koden.  
* Flere prosedyrer som bare ble brukt lokalt og bare var ment å brukes lokalt, var ikke merket som lokale.  
* De fleste prosedyrene hadde ingen parametere og brukte globale variabler. Noen brukte parametere og overstyrte globale variabler med lokale.  
* Kodemønstre for å søke i finanskonti og opprette finansposter og mva-poster var ikke standardisert og varierte fra sted til sted. I tillegg var det mye duplisering av kode og brutt symmetri mellom kunde- og leverandørkode.  
* En stor del av koden i kodeenhet 12, omtrent 30 prosent, er knyttet til kontantrabatt og toleranseberegninger, selv om disse funksjonene ikke er nødvendige i mange land og regioner.  
* Bokføring, Utlign, Opphev utligning, Tilbakefør, Kontantrabatt, Betalingstoleranse og Valutakursjustering var tilknyttet i kodeenhet 12 ved hjelp av en lang liste med globale variabler.  
  
### <a name="new-architecture"></a>Ny arkitektur  
Kodeenhet 12 har fått følgende forbedringer i [!INCLUDE[d365fin](includes/d365fin_md.md)]:  
  
* Kodeenhet 12 er refaktorert til mindre prosedyrer (alle er færre enn 100 kodelinjer).  
* Standardiserte mønstre for søk i finanskonti er implementert ved hjelp av hjelperfunksjoner fra Bokføringsgruppe-tabeller.  
* Et rammeverk for bokføringsmotor er implementert for å behandle starten og slutten på transaksjoner og isolere opprettelsen av finansposter og mva-poster, innsamlingen av mva-justering og beregningen av flere valutabeløp.  
* Duplisering av kode er eliminert.  
* Mange hjelperfunksjoner er overført til tilsvarende tabeller for kunde- og leverandørposter.  
* Bruken av globale variabler er minimert, slik at hver prosedyre bruker parametere og kapsler inn sin egen programlogikk.  
  
## <a name="see-also"></a>Se også  
[Designdetaljer: Strukturen til bokføringsgrensesnittet](design-details-posting-interface-structure.md)   
[Designdetaljer: Strukturen til bokføringsmotoren](design-details-posting-engine-structure.md)
