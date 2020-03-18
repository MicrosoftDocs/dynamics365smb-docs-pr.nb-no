---
title: Revidere endringer | Microsoft Docs
description: Du kan aktivere en brukerlogg slik at du har en logg over eventuelle endringer i data i sporede tabeller. Du kan også spore aktiviteter med bestemte typer aktivitetslogger.
author: edupont04
ms.service: dynamics365-business-central
ms.topic: get-started-article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: user log, user activity, tracking
ms.date: 10/01/2019
ms.author: edupont
ms.openlocfilehash: cb091a54b7b8da571117c807a621ed298842444c
ms.sourcegitcommit: d0dc5e5c46b932899e2a9c7183959d0ff37738d6
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 02/20/2020
ms.locfileid: "3076662"
---
# <a name="auditing-changes-in-business-central"></a>Revidere endringer i Business Central

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

## <a name="working-with-activity-logs"></a>Arbeide med aktivitetslogger

Fra enkelte sider i [!INCLUDE [prodshort](includes/prodshort.md)] kan du vise en aktivitetslogg som viser statusen og eventuelle feil fra filer du eksporterer fra eller importerer til [!INCLUDE [prodshort](includes/prodshort.md)].  

Informasjonen vises på **Aktivitetslogg**-siden i samsvar med konteksten den åpnes i. Du kan åpne vinduet fra sidene **Oppsett av dokumentutvekslingstjeneste**, **Innkommende dokument**, **Bokført salgsfaktura**og **Bokført salgskreditnota** , for eksempel. Du kan tømme oversikten over loggposter eller bare fjerne oversikten over poster som er eldre enn 7 dager.  

## <a name="see-also"></a>Se også
[Endre grunnleggende innstillinger](ui-change-basic-settings.md)  
[Sortere, søke etter og filtrere](ui-enter-criteria-filters.md)  
[Finne sider og informasjon med Fortell meg](ui-search.md)  
[Tilordne tillatelser til brukere og grupper](ui-define-granular-permissions.md)    
[Arbeide med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)  
