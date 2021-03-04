---
title: Designdetaljer – Varesporing og planlegging | Microsoft Docs
description: Siden de lagres i reservasjonssystemet, er varesporingsnumre fullstendig koordinert med ordresporingsposter.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: 4f9fd9287055bed116201d13417a6a392cf9b477
ms.sourcegitcommit: ddbb5cede750df1baba4b3eab8fbed6744b5b9d6
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 10/01/2020
ms.locfileid: "3927000"
---
# <a name="design-details-item-tracking-and-planning"></a>Designdetaljer: Varesporing og planlegging
Siden de lagres i reservasjonssystemet, er varesporingsnumre fullstendig koordinert med ordresporingsposter. Dette betyr at varer med sporingsposter kan få tilordnet varesporingsnumre. I motsetning kan varer med varesporingsnumre bli sporingsposter. Hvis du vil ha mer informasjon, kan du se [Designdetaljer: Varesporingsutforming](design-details-item-tracking-design.md).

Hvis du vil ha mer informasjon om de integrerte systemene, kan du se [Designdetaljer: Reservasjon, ordresporing og handlingsmeldinger](design-details-reservation-order-tracking-and-action-messaging.md).

Siden ordresporingen bare gjelder bestemt vareutligning, gjelder koordineringen med varesporingsnumrene bare for varer som er konfigurert til å bruke bestemt varesporing. Dette angis i feltene **Sporing basert på s.nr.** og **Sporing basert på parti** på varekortet, som angir følgende:

- Varen må ha et serienummer eller partinummer når den bokføres.
- Varen må gjelde for samme serienummer eller partinummer når den bokføres som utgående.

I tråd med standard motkontoprinsipper for forsyning/etterspørsel vil planleggingssystemet og den tilknyttede ordresporingsfunksjonen bare samsvare forsyning og behov med varesporingsnumre hvis den aktuelle varen bruker spesifikk varesporing. I alle andre tilfeller ignorerer planleggings- og ordresporingssystemer varesporingsnumre når de bruker forsyning til å dekke behov, eller bruker behov for forsyning. Hvis du vil ha mer informasjon, kan du se [Designdetaljer: Reservasjon, ordresporing og handlingsmeldinger](design-details-reservation-order-tracking-and-action-messaging.md).

Når det for eksempel finnes ordresporing for en bestemt vare, betyr dette at poster for varen allerede finnes i tabellen **Reservasjonspost**, som er kjernen i reservasjonssystemet, før det angis varesporingsnumre. Derfor gjelder følgende koblingsbegrensninger for varesporingsnumrene som skal spores:

- Behov med serie- eller partinummer kan bare dekke forsyning med samme serie- eller partinummer.
- Behov uten serie- eller partinummer kan dekke alle forsyninger med eller uten samme serie- eller partinummer.

I tillegg til sine konsekvenser for dynamisk sporing vil ikke koblingsbegrensningene for varesporing påvirke planleggingssystemet i betydelig grad.

På forsyningssiden blir det vanligvis ikke angitt et serie- eller partinummer før umiddelbart før ordren bokføres, for eksempel et kjøpsmottak på lageret. Når du registrerer et serie- eller partinummer på behovssiden, for eksempel i en ordre, er dette serie- eller partinummeret allerede på lager. Varesporingsnumre er derfor vanligvis ikke et problem i forsyningsplanlegging.

Alle behov med serie- eller partinumre må samsvare med tilsvarende forsyning for varer som bruker bestemt varesporing. I de fleste tilfeller er det ikke fornuftig å gjenbestille et bestemt serie- eller partinummer, og planlegging av kjøp eller produksjonsutstyr blir sannsynligvis ikke påvirket. Under overføring av varer fra én lokasjon til en annen, er det imidlertid sannsynlig at overføringen er for et bestemt parti, så planlegging av overføring av forsyninger kan bli påvirket av bestemte koblingsbegrensninger.

Hvis du vil ha mer informasjon, kan du se [Designdetaljer: Overføringer i planlegging](design-details-transfers-in-planning.md).

## <a name="balancing-demand-and-supply"></a>Balansere behov og forsyning
Hvis en vare krever en bestemt varesporing, opprettes det en sporingskobling fra varesporingsbehov for alle varene til eventuell tilsvarende varesporingsforsyning, og den eneste begrensningen er at forsyningen må komme før behovet. Hvis det i disse tilfellene ikke finnes varesporingsforsyning som tilsvarer spesifikke varesporingsbehov, vil det umiddelbart bli opprettet en ny varesporingsforsyning uten å ta hensyn til ordreskalering, planleggingsparametere eller ny planlegging av eksisterende forsyning av samme serie- eller partinummer.

Hvis det er tilordnet varesporingsnumre på behovs- eller forsyningssiden uten å kreve bestemt varesporing, vil det bli opprettet en sporingskobling fra behovet til forsyningen basert på best egnede tidsberegning og antall, som i vanlig fremgangsmåte for balansering. Det angitte varesporingsnummeret går inn i sporingsposten på samme måte som et hvilket som helst angitt varesporingsantall definerer den ene enden av sporingskoblingen. Dette betyr at varesporingsnummeret som angis, beholdes så lenge det også er en del av sporingsposten.

Hvis varesporingsnumre tilordnes på forsyningssiden uten å kreve bestemt varesporing, betraktes forsyningen som fast av planleggingssystemet. Ingen endring av størrelse eller ny planlegging blir foreslått for denne forsyningen, men det tas hensyn til forsyningen når planleggingssystemet prøver å dekke bruttobehovene.

Hvis du vil ha mer informasjon, kan du se [Designdetaljer: Balansere behov og forsyning](design-details-balancing-demand-and-supply.md).  

## <a name="see-also"></a>Se også  
[Designdetaljer: Varesporingsutforming](design-details-item-tracking-design.md)  
[Designdetaljer: Balansere behov og forsyning](design-details-balancing-demand-and-supply.md)  
[Designdetaljer: Reservasjon, ordresporing og handlingsmeldinger](design-details-reservation-order-tracking-and-action-messaging.md)   
[Designdetaljer: Forsyningsplanlegging](design-details-supply-planning.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]