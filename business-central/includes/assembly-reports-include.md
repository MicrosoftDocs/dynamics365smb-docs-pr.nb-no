---
author: edupont04
ms.topic: include
ms.date: 04/01/2021
ms.author: edupont
ms.openlocfilehash: 13d4e619c738b509258b7954d2ce035365f66e75
ms.sourcegitcommit: cdb57f14960f58b1d36a1b373fbf35dfed5fad9e
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 02/23/2022
ms.locfileid: "8334827"
---
Tabellen nedenfor beskriver noen av nøkkelrapportene i monteringsrapportering.

| Rapport | Beskrivelse | ID | 
|---------|---------|---------|
| [Monteringsstykklister](https://businesscentral.dynamics.com?report=801)|Viser en oversikt over stykklister: navn, stykklistenummer, stykklistekomponenter og alle andre stykklister som er en del av Stykkliste. Stykklistekomponentene er definert i tabellen Stykklistekomponent. Her vil du også se enheten og det nødvendige antallet for hver enkelt komponent per lagerenhet. |801|
| [Vare – kan lage (tid)](https://businesscentral.dynamics.com?report=5871)|Viser hvordan fem forskjellige sentrale tilgjengelighetstall endres over tid for en stykklistevare. Disse tallene endres i henhold til forventede forsynings- og behovshendelser og forsyning som er basert på tilgjengelige komponenter som kan monteres eller produseres.<br>Du kan bruke rapporten for å finne ut om du kan oppfylle en ordre for en vare på en angitt dato. Du gjør dette ved å se på varens gjeldende tilgjengelighet i kombinasjon med de potensielle antallene av varens komponenter som kan leveres hvis en monteringsordre ble startet. Rapporten viser når og hvor mange enheter av en monterings- og produksjonsvare du kan produsere basert på komponenttilgjengelighet og varens nåværende tilgjengelighet. Dette vises som totalantallet.<br>Informasjonen vises i et diagram der hvert tilgjengelighetstall er en linje som løper langs tidslinjen og beveger seg opp eller ned når antallene endrer seg. Tallene kommer fra den samme motoren som gir informasjon til vinduet **Varetilgjengelighet etter stykklistenivå**. |5871|
| [Stykklistekostandeler – fordeling](https://businesscentral.dynamics.com?report=5872)|Viser hvordan kostnadene for en montert eller produsert vare er fordelt gjennom stykklisten.<br>Slik informasjon kan være nyttig når du for eksempel skal bestemme om du vil bytte komponentleverandører, erstatte internt kapasitetsforbruk med arbeidskraft som er satt ut, eller omvendt, eller når du gjennomgår og endrer stykklisten for en vare.<br>Det første diagrammet i rapporten viser total enhetskost for den overordnede varens komponenter og arbeidsressurser inndelt i opptil fem ulike kostandeler, presentert grafisk og med ulike farger.<br>Sektordiagrammet som heter *Etter materiale/arbeid*, viser proporsjonal fordeling mellom den overordnede varens materiale og arbeidskostnader, i tillegg til egen indirekte produksjonskost. Materialkostandelen omfatter varens materialkost. Arbeidskostandelen inkluderer kapasitet, indirekte kapasitetskostnader og underleveransekostnader. Kostandelene vises på en annen måte avhengig av valgene i feltet **Vis bare**.<br>Sektordiagrammet som heter *Etter direkte/indirekte*, viser proporsjonal fordeling mellom den overordnede varens direkte og indirekte kostnader. Direkte kostnadsandel omfatter varens materiale, kapasitet og underleveransekostnader. Indirekte kostnadsandel omfatter indirekte kapasitetskostnader og indirekte produksjonskostnader.<br>Tabellen nederst i rapporten er inkludert når du merker av for Inkluder detaljer. Den viser valgte verdier fra vinduet Stykklistekostandeler etter enkeltnivå eller opprullert, avhengig av hvilket alternativ du velger i feltet Vis kostandeler som.|5872|
| [Inngår-i-liste](https://businesscentral.dynamics.com?report=809)|Viser en oversikt over hvilke stykklister som de valgte varene inngår i. En nyttig oversikt i tilfelle du må endre en komponent i en stykkliste som er satt inn i en monteringsvare. Hvis leverandøren for eksempel ikke lenger kan levere en bestemt vare som du brukte for monteringen/produksjonen. I slike scenarioer gir denne rapporten en enkel oversikt over hvilke stykklister komponenten inngår i. Du kan definere et filter for nummeret på komponenten.|809|
| [Stykkliste – råvarer](https://businesscentral.dynamics.com?report=810)|Denne rapporten kan gi deg en oversikt over komponentene som trengs, både for montering og produksjon. Du ser lageret, lagerenhetskoden, hovedleverandøren hvis feltet Leverandørnr. skrives inn i selve varekortet, og beregningen av leveringstid.|810|
| [Stykkliste – halvfabrikata](https://businesscentral.dynamics.com?report=811)|Hvis du produserer eller monterer halvfabrikater, bruker du denne rapporten til å få en oversikt over denne komponenttypen. Denne rapporten viser lagerenheten, lageret, enhetskostnadene og et alternativt varenummer. |811|
| [Monteringsstykkliste – sluttvarer](https://businesscentral.dynamics.com?report=812)|Viser en oversikt over varer eller stykklister som ikke er stykklistekomponenter. **Obs**! Denne rapporten er ikke begrenset til stykkliste, så husk derfor å angi filter i feltene **Monteringsstykkliste** eller **Etterfyllingssystem**|812|
| [Montere til ordre – salg](https://businesscentral.dynamics.com?report=915)|Viser nøkkelsalgstall for monteringskomponentvarer som kan selges som en del av en montering i monter-til-ordre-salg og som en egen vare direkte fra lageret.<br>Bruk denne rapporten til å analysere tallene i antall, kostnader, salg og fortjeneste for monteringskomponenter for å støtte beslutninger, for eksempel om et sett skal få ny pris, eller om du skal begynne eller slutte å bruke en bestemt vare i monteringer.<br>Raden **Til montering** viser salgstallene for det totale antallet som er solgt som en del av en monteringsvare. Det bestemte monteringsvaresalget som summerer opp denne totalen, vises hvis du velger feltet **Vis monteringsdetaljer**.<br>Fokuset er på monteringskomponentene, men tallene beregnes fra fortjenestemarginen for den overordnede varen, dvs. monteringsvaren. Salgsbeløpet for hver komponent beregnes på samme måte fra sin egen kostnad og dekningsgraden for den overordnede i følgende formel.<br>Rapporten viser informasjon for varene som oppfyller ett eller begge kriteriene nedenfor:<br>- Finnes i monteringsstykklisten for en vare som bruker monteringsprinsippet Montere til ordre.<br>- Har blitt solgt som en del av montere-til-ordre-salg.|915|