---
title: "Designdetaljer – Vindu for varesporingslinjer | Microsoft-dokumentasjon"
description: Les om hvordan du administrerer flyten av serie- og partinumre i lageret.
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: design, inventory, item, tracking, serial number, lot number
ms.date: 07/01/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 2c13559bb3dc44cdb61697f5135c5b931e34d2a8
ms.openlocfilehash: 62070ef4e580a3bd665130c9b017bf164bbe2142
ms.contentlocale: nb-no
ms.lasthandoff: 09/22/2017

---
# <a name="design-details-item-tracking-lines-window"></a>Designdetaljer: Vindu for varesporingslinjer
Varesporings- og reservasjonsposter opprettes i reservasjonssystemet, og tilgjengeligheten beregnes dynamisk. Data som skrives inn i vinduet **Varesporingslinjer**, behandles i en midlertidig versjon av tabellen **Sporingsspesifikasjon**. Når vinduet lukkes, lagres de aktive dataene i **Reservasjonspost**-tabellen, og historiske dataene lagres i **Sporingsspesifikasjon**-tabellen. Hvis du vil ha mer informasjon, se [Designdetaljer: Aktive kontra historiske varesporingsposter](design-details-active-versus-historic-item-tracking-entries.md).  
  
Oppslag fra feltene **Serienr.** og **Partinr.** viser tilgjengelighet basert på tabellen **Varepost** og **Reservasjonspost**, uten noe datofilter. Matrisen over antallsfelt i hodet i vinduet **Varesporingslinjer** gir en dynamisk oversikt over antallene og summene til varesporingsnumrene som skrives inn på linjene i vinduet. Antallene må svare til antallene på bilagslinjen, som er angitt med **0** i **Udefinert**-feltet i hodet i vinduet.  
  
For å koordinere flyten av serie- og partinumre gjennom lageret gjelder følgende regler ved registrering av data i vinduet **Varesporingslinjer**:  
  
* For både innkommende og utgående varesporingslinjer kan du ikke angi et serienummer, med eller uten et partinummer, flere ganger i samme forekomst av vinduet **Varesporingslinjer**. Hvis du prøver å skrive inn en kombinasjon av serie- eller partinumre som allerede finnes i vinduet, sperrer en feilmelding for dataregistrering.  
* Du kan ikke bokføre relatert dokument for inngående sporingslinjer hvis en vare av samme variant og med samme serienummer allerede finnes på lageret. Hvis du prøver å bokføre en positiv linje for en lagervare med samme variant og serienummer, sperrer en feilmelding for bokføringen. For innkommende og utgående varesporingslinjer i åpne dokumenter, kan du imidlertid ha samme kombinasjon av serie- eller partinumre som er relatert til forskjellige kildedokumentlinjer, det vil si finnes i ulike forekomster av vinduet **Varesporingslinjer** til det tilknyttede dokumentet er bokført.  
* Hvis varen er konfigurert for sporing av spesifikt serie- eller partinummer, kan du ikke bokføre en linje i det utgående dokumentet, med mindre en vare med angitt serie- eller partinummer finnes på lageret. Hvis du prøver å bokføre en linje i et utgående dokument for en vare med et partinummer som ikke finnes på lager, sperrer en feilmelding for bokføringen.  
  
Reglene for registrering av data i vinduet **Varesporingslinjer** støtter også koplingsprinsippene som styrer sporing, planlegging og reservasjon. Hvis du vil ha mer informasjon, kan du se [Designdetaljer: Varesporing og planlegging](design-details-item-tracking-and-planning.md).  
  
## <a name="see-also"></a>Se også  
[Designdetaljer: Varesporing](design-details-item-tracking.md)
