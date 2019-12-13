---
title: Designdetaljer – Varesporing i lageret | Microsoft-dokumentasjon
description: Håndtering av serie- og partinumre er hovedsakelig en lageroppgave, og derfor har alle inngående og utgående lagerdokumenter standard funksjonalitet for tilordning og valg av varesporingsnumre. Siden reservasjonssystemet er basert på vareposter, blir imidlertid ikke lageraktivitetsdokumenter som registrerer bare lagerposter, støttet fullstendig.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: design, item, tracking, serial number, lot number, outbound documents
ms.date: 10/01/2019
ms.author: sgroespe
ms.openlocfilehash: b7fdb0d6495f1512e1ab3bf80eb76a5dad9d87e5
ms.sourcegitcommit: cfc92eefa8b06fb426482f54e393f0e6e222f712
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 12/03/2019
ms.locfileid: "2880187"
---
# <a name="design-details-item-tracking-in-the-warehouse"></a>Designdetaljer: Varesporing på lageret
Håndtering av serie- og partinumre er hovedsakelig en lageroppgave, og derfor har alle inngående og utgående lagerdokumenter standard funksjonalitet for tilordning og valg av varesporingsnumre.  

Siden reservasjonssystemet er basert på vareposter, blir imidlertid ikke lageraktivitetsdokumenter som registrerer bare lagerposter, støttet fullstendig. Siden reservasjoner og varesporingsnumre bare kan behandles på lokasjonsnivå og ikke på hylle/ og sonenivå, kan ikke siden **Varesporingslinjer** åpnes fra lageraktivitetsdokumenter. Det samme gjelder for **Reservasjon**-siden.  

Etter at et serie- eller partinummer er lagt til en vare på lagerlokasjonen, kan de flyttes og omklassifiseres fritt i lageret ved hjelp av en uavhengig struktur for varesporings som ikke er relatert til reservasjonssystemet. Du har direkte tilgang til feltene **Serienr.** og **Partinr.** på lagerdokumentlinjer. Når serie- eller partinummeret senere er med i utgående bokføring, synkroniseres det med reservasjonssystemet som en del av vanlig hyllejustering. Hvis du vil ha mer informasjon, kan du se [Designdetaljer: Integrasjon med lagerbeholdning](design-details-integration-with-inventory.md).  

Reservasjonssystemet tar imidlertid hensyn til lageraktiviteter ved beregning av tilgjengelighet. Varer som for eksempel er tildelt plukkinger eller registrert som plukket, kan ikke reserveres. Hvis du vil ha mer informasjon, kan du se [Designdetaljer: Tilgjengelighet i lageret](design-details-availability-in-the-warehouse.md).

## <a name="see-also"></a>Se også  
[Designdetaljer: Varesporing](design-details-item-tracking.md)  
[Designdetaljer: Integrasjon med lagerbeholdning](design-details-integration-with-inventory.md)  
[Designdetaljer: Tilgjengelighet i lageret](design-details-availability-in-the-warehouse.md)  
[Designdetaljer: Varesporingsutforming](design-details-item-tracking-design.md)
