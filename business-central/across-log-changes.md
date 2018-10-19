---
title: Spore brukeraktivitet i en endringsloggen | Microsoft-dokumentasjon
description: Du kan aktivere en brukerlogg slik at du har en logg over eventuelle endringer i data i sporede tabeller.
author: edupont04
ms.service: dynamics365-business-central
ms.topic: get-started-article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: user log, user activity, tracking
ms.date: 10/01/2018
ms.author: edupont
ms.translationtype: HT
ms.sourcegitcommit: 9dbd92409ba02281f008246194f3ce0c53e4e001
ms.openlocfilehash: ab9696a3cc14970def764b2741d50dbcd5207460
ms.contentlocale: nb-no
ms.lasthandoff: 09/28/2018

---
# <a name="logging-changes-in-business-central"></a>Logge endringer i Business Central
Du kan aktivere endringsloggen i [!INCLUDE[d365fin](includes/d365fin_md.md)], slik at du har en historikk for aktivitetene. Loggen er basert på endringene som utføres på dataene i tabellene som du vil spore. I endringsloggen er oppføringene ordnet kronologisk og viser endringer som gjøres i feltene i de angitte tabellene. Endringsloggen samler inn alle endringer som utføres i tabellen.  

## <a name="working-with-the-change-log"></a>Arbeide med endringsloggen
Et vanlig problem i mange finanssystemer er å lokalisere opphavet til feil og endringer i dataene. Det kan være alt fra et uriktig kundetelefonnummer til uriktig bokføring i finanspostene. Ved hjelp av endringsloggen kan du spore alle direkte endringer som brukeren gjør i dataene i databasen. For må angi hver tabell og hvert felt du vil at systemet skal logge. Deretter må du aktivere endringsloggen.  

Du kan aktivere eller deaktivere endringsloggen i vinduet **Endringsloggoppsett**. Når du aktiverer eller deaktiverer endringsloggen, logges denne aktiviteten, slik at du alltid kan se hvilken bruker som deaktiverte eller aktiverte endringsloggen. Denne funksjonen kan ikke slås av.  

I vinduet **Endringsloggoppsett**, hvis du velger **Tabeller**-handlingen, kan du angi hvilke tabeller du vil spore endringer for, og hvilke endringer du vil spore. [!INCLUDE[d365fin](includes/d365fin_md.md)] sporer også flere systemtabeller.

Når du har opprettet endringsloggen, aktivert den og endret data, kan du vise og filtrere endringene i vinduet **Endringsloggposter**. Hvis du vil slette postene, kan du gjøre det i vinduet **Slett endringsloggposter**, der du kan definere filtre basert på datoene og tidspunktene.  

## <a name="see-also"></a>Se også
[Endre grunnleggende innstillinger](ui-change-basic-settings.md)  
[Sortering](ui-sorting.md)  
[Bruke Søk etter side eller rapport](ui-search.md)  
[Administrere brukere og tillatelser](ui-how-users-permissions.md)    
[Arbeide med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)  

