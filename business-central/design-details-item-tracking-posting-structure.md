---
title: Designdetaljer – Bokføringsstruktur for varesporing
description: Lær hvordan du bruker vareposter som den hovedbærer av varesporingsnumre i Bokføringsstruktur for varesporing.
author: brentholtorf
ms.topic: conceptual
ms.devlang: al
ms.search.keywords: 'design, item tracking, posting, inventory'
ms.date: 06/15/2021
ms.author: bholtorf
ms.service: dynamics-365-business-central
ms.reviewer: bholtorf
---
# <a name="design-details-item-tracking-posting-structure"></a>Designdetaljer: Bokføringsstruktur for varesporing
Vareposter brukes som hovedbærere av varesporingsnumre, slik at de passer med funksjonene for kostberegning for beholdning og gir en enklere og mer robust løsning.  
  
Varesporingsnumre i ordrenettverksenheter og ikke-ordrenettverksenheter er angitt i tabellen **Reservasjonspost** (T337). Varesporingsnumre som er knyttet til historisk informasjon, blir hentet direkte fra vareposter som er knyttet til den aktuelle transaksjonen. Dette betyr at vareposter gjenspeiler varesporingsspesifikasjonen for den bokførte ordrelinjen.  
  
Siden **Varesporingslinjer** henter informasjonen fra T337 og varepostene og viser den via den midlertidige tabellen **Sporingsspesifikasjon** (T336). T336 inneholder også de midlertidige dataene på siden **Varesporingslinjer** for varesporingsantall som skal faktureres.  
  
## <a name="one-to-many-relation"></a>Én-til-mange-relasjon
Tabellen **Vareposttilknytning**, som brukes til å koble en bokført dokumentlinje til de tilknyttede varepostene, består av to hoveddeler:  
  
* En peker til den posterte dokumentlinjen, **Ordrelinjenr.**-feltet .  
* Et løpenummer peker til en varepost, feltet **Vareløpenr.**.  
  
Funksjonaliteten til det eksisterende **Postnr.**-feltet, som knytter en varepost til en bokført dokumentlinje, håndterer den vanlige én-til-én-relasjonen når ingen varesporingsnumre er på den bokførte dokumentlinjen. Hvis det finnes varesporingsnumre, vil **Løpenummer**-feltet forbli tomt, og en-til-mange-relasjonen behandles av tabellen **Vareposttilknytning**. Hvis den bokførte dokumentlinjen inneholder varesporingsnumre, men bare er knyttet til en enkelt varepost, vil **Løpenummer**-feltet håndterer tilknytningen, og ingen oppføringen blir opprettet i tabellen **Vareposttilknytning**.  
  
## <a name="codeunits-80-and-90"></a>Kodeenhet 80 og 90
For å få varepostene delt ved bokføring omsluttes koden i kodeenhet 80 og kodeenhet 90 med løkker som går gjennom globale, midlertidige postvariabler. Denne koden kaller kodeenhet 22 med en varekladdelinje. Disse variablene initialiseres når varesporingsnumre finnes for dokumentlinjen. Denne sløyfestrukturen brukes alltid for å holde koden enkel. Hvis det ikke finnes varesporingsnumre for dokumentlinjen, vil det settes inn en enkeltpost, og løkken kjøres bare én gang.  
  
## <a name="posting-the-item-journal"></a>Bokføre varekladden
Varesporingsnumre overføres via reservasjonspostene som er knyttet til vareposten, og gjennomgang av varesporingsnumre foretas i kodeenhet 22. Dette konseptet fungerer på samme måte som når en varekladdelinje indirekte brukes til å bokføre et salg eller en bestilling som når en varekladdelinje brukes direkte. Når varekladden brukes direkte, peker feltet **Kilderad-ID** mot selve varekladdelinjen.  
  
## <a name="code-unit-22"></a>Kodeenhet 22
Kodeenhet 80 og 90 går gjennom kodeenhet 22-kall under fakturabokføring av varesporingsnumre og under fakturering av eksisterende leveringer og mottak.  
  
Under antallsbokføring av varesporingsnumre, henter kodeenhet 22 varesporingsnumre fra postene i T337 som er knyttet til posteringen. Disse postene plasseres direkte på varekladdelinjen.  
  
Kodeenhet 22 går gjennom varesporingsnumrene og deler opp posteringen i de respektive varepostene som inneholder varesporingsnumrene. Informasjon om hvilke vareposter som opprettes, returneres til T337 ved hjelp av en midlertidig T336-post, som kalles opp av en prosedyre i kodeenhet 22. Dette utløses når kodeenhet 22 har fullført sin kjøring, fordi på dette tidspunktet inneholder kodeenhet 22-objektet informasjonen. Når den midlertidige T336-posten hentes, oppretter kodeenhet 80 og 90 poster i tabellen **Vareposttilknytning** for å knytte de opprettede varepostene til den opprettede følgeseddel- eller mottakslinjen. Kodeenhet 80 eller 90 konverterer deretter de midlertidige T336-postene til virkelige T336-poster som er knyttet til den aktuelle linjen. Denne konverteringen skjer imidlertid bare hvis den bokførte dokumentlinjen ikke slettes, fordi den er bare delvis bokført.  
  
## <a name="see-also"></a>Se også
[Designdetaljer: Varesporing](design-details-item-tracking.md)   
[Designdetaljer: Varesporingsutforming](design-details-item-tracking-design.md)

[!INCLUDE[footer-include](includes/footer-banner.md)]
