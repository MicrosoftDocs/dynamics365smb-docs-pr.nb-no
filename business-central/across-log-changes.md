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
ms.date: 11/14/2018
ms.author: edupont
ms.translationtype: HT
ms.sourcegitcommit: 33b900f1ac9e295921e7f3d6ea72cc93939d8a1b
ms.openlocfilehash: 2a95e770f0b78732723ba0d9db5d343a3ed3a97f
ms.contentlocale: nb-no
ms.lasthandoff: 11/26/2018

---
# <a name="logging-changes-in-business-central"></a>Logge endringer i Business Central

Du kan aktivere endringsloggen i [!INCLUDE[d365fin](includes/d365fin_md.md)], slik at du har en historikk for aktivitetene. Loggen er basert på endringene som utføres på dataene i tabellene som du vil spore. På siden **Endringsloggposter** er oppføringene ordnet kronologisk og viser endringer som gjøres i feltene i de angitte tabellene. Endringsloggen samler inn alle endringer som utføres i tabellen.

> [!Important]
> En brukers endringer vises ikke i **Endringsloggposter** før brukerøkten startes på nytt, som skjer i følgende tilfeller:
<br />
> * Økten har utløpt og ble oppdatert.
> * Brukeren har valgt et annet selskap eller rollesenter.
> * Brukeren logget ut og inn igjen.

## <a name="working-with-the-change-log"></a>Arbeide med endringsloggen

Et vanlig problem i mange finanssystemer er å lokalisere opphavet til feil og endringer i dataene. Det kan være alt fra et uriktig kundetelefonnummer til uriktig bokføring i finanspostene. Ved hjelp av endringsloggen kan du spore alle direkte endringer som brukeren gjør i dataene i databasen. For må angi hver tabell og hvert felt du vil at systemet skal logge. Deretter må du aktivere endringsloggen.  

Du kan aktivere eller deaktivere endringsloggen på siden **Endringsloggoppsett**. Når en bruker aktiverer eller deaktiverer endringsloggen, logges denne aktiviteten, slik at du alltid kan se hvilken bruker som deaktiverte eller aktiverte endringsloggen.

På siden **Endringsloggoppsett**, hvis du velger **Tabeller**-handlingen, kan du angi hvilke tabeller du vil spore endringer for, og hvilke endringer du vil spore. [!INCLUDE[d365fin](includes/d365fin_md.md)] sporer også flere systemtabeller.

Når du har opprettet endringsloggen, aktivert den og endret data, kan du vise og filtrere endringene på siden **Endringsloggposter**. Hvis du vil slette postene, kan du gjøre det på siden **Slett endringsloggposter**, der du kan definere filtre basert på datoene og tidspunktene.  

## <a name="see-also"></a>Se også
[Endre grunnleggende innstillinger](ui-change-basic-settings.md)  
[Sortering](ui-sorting.md)  
[Bruke Søk etter side eller rapport](ui-search.md)  
[Administrere brukere og tillatelser](ui-how-users-permissions.md)    
[Arbeide med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)  

