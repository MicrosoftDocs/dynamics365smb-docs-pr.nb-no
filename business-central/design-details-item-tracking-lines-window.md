---
title: Designdetaljer – Side for varesporingslinjer | Microsoft-dokumentasjon
description: Les om hvordan du administrerer flyten av serie- og partinumre i lageret.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: design, inventory, item, tracking, serial number, lot number
ms.date: 04/01/2019
ms.author: sgroespe
ms.openlocfilehash: 0ddfa9b2d981f81f649240a08c26e8cca845bd1f
ms.sourcegitcommit: 60b87e5eb32bb408dd65b9855c29159b1dfbfca8
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 04/29/2019
ms.locfileid: "1246132"
---
# <a name="design-details-item-tracking-lines-page"></a>Designdetaljer: Side for varesporingslinjer
Varesporings- og reservasjonsposter opprettes i reservasjonssystemet, og tilgjengeligheten beregnes dynamisk. Data som skrives inn på siden **Varesporingslinjer**, behandles i en midlertidig versjon av tabellen **Sporingsspesifikasjon**. Når siden lukkes, lagres de aktive dataene i **Reservasjonspost**-tabellen, og historiske dataene lagres i **Sporingsspesifikasjon**-tabellen. Hvis du vil ha mer informasjon, se [Designdetaljer: Aktive kontra historiske varesporingsposter](design-details-active-versus-historic-item-tracking-entries.md).  
  
Oppslag fra feltene **Serienr.** og **Partinr.** viser tilgjengelighet basert på tabellen **Varepost** og **Reservasjonspost**, uten noe datofilter. Matrisen over antallsfelt i hodet på siden **Varesporingslinjer** gir en dynamisk oversikt over antallene og summene til varesporingsnumrene som skrives inn på linjene på siden. Antallene må svare til antallene på bilagslinjen, som er angitt med **0** i **Udefinert**-feltet i hodet på siden.  
  
For å koordinere flyten av serie- og partinumre gjennom lageret gjelder følgende regler ved registrering av data på siden **Varesporingslinjer**:  
  
* For både innkommende og utgående varesporingslinjer kan du ikke angi et serienummer, med eller uten et partinummer, flere ganger i samme forekomst av siden **Varesporingslinjer**. Hvis du prøver å skrive inn en kombinasjon av serie- eller partinumre som allerede finnes på siden, sperrer en feilmelding for dataregistrering.  
* Du kan ikke bokføre relatert dokument for inngående sporingslinjer hvis en vare av samme variant og med samme serienummer allerede finnes på lageret. Hvis du prøver å bokføre en positiv linje for en lagervare med samme variant og serienummer, sperrer en feilmelding for bokføringen. For innkommende og utgående varesporingslinjer i åpne dokumenter, kan du imidlertid ha samme kombinasjon av serie- eller partinumre som er relatert til forskjellige kildedokumentlinjer, det vil si finnes i ulike forekomster av siden **Varesporingslinjer** til det tilknyttede dokumentet er bokført.  
* Hvis varen er konfigurert for sporing av spesifikt serie- eller partinummer, kan du ikke bokføre en linje i det utgående dokumentet, med mindre en vare med angitt serie- eller partinummer finnes på lageret. Hvis du prøver å bokføre en linje i et utgående dokument for en vare med et partinummer som ikke finnes på lager, sperrer en feilmelding for bokføringen.  
  
Reglene for registrering av data på siden **Varesporingslinjer** støtter også koplingsprinsippene som styrer sporing, planlegging og reservasjon. Hvis du vil ha mer informasjon, kan du se [Designdetaljer: Varesporing og planlegging](design-details-item-tracking-and-planning.md).  
  
## <a name="see-also"></a>Se også  
[Designdetaljer: Varesporing](design-details-item-tracking.md)