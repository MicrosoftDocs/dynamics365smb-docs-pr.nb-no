---
title: Produksjonsrapporter og analyser
description: Se hvilke produksjonsrapporter og analyser som er tilgjengelige i standardversjonen av Business Central, slik at du kan holde oversikt over virksomheten.
author: AndreiPanko
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.search.keywords: reporting
ms.date: 06/01/2021
ms.author: andreipa
ms.openlocfilehash: 0cacf41f0a055267af5b0ce5a8b68b34d86a1cb5
ms.sourcegitcommit: 0953171d39e1232a7c126142d68cac858234a20e
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 06/09/2021
ms.locfileid: "6216382"
---
# <a name="production-reports-and-analytics-in-business-central"></a>Produksjonsrapporter og analyser i Business Central

Produksjonsrapportering i [!INCLUDE [prod_short](includes/prod_short.md)] gjør det mulig for produksjons- og forretningsfolk å få innsikt og statistikk om gjeldende og tidligere produksjonsaktiviteter.  

## <a name="reports"></a>Rapporter

Tabellen nedenfor beskriver noen av nøkkelrapportene i produksjonsrapportering.

|Rapport |Objekt-ID|Beskrivelse  |
|---------|---------|---------|
|**Antallsutfoldelse av stykkl.**|99000753|Viser en innrykket stykklisteoversikt for varen eller varene du angir i filtrene. Produksjonsstykklisten er fullstendig utfoldet for alle nivåene.|
|**Vare – kan lage (tid)**|5871|Viser hvordan fem forskjellige sentrale tilgjengelighetstall endres over tid for en stykklistevare. Disse tallene endres i henhold til forventede forsynings- og behovshendelser og forsyning som er basert på tilgjengelige komponenter som kan monteres eller produseres.<br>Du kan bruke rapporten for å finne ut om du kan oppfylle en ordre for en vare på en angitt dato. Du gjør dette ved å se på varens gjeldende tilgjengelighet i kombinasjon med de potensielle antallene av varens komponenter som kan leveres hvis en monteringsordre er startet. Rapporten viser når og hvor mange enheter av en monterings- og produksjonsvare du kan produsere basert på komponenttilgjengelighet og varens nåværende tilgjengelighet. Dette vises som totalantallet.<br>Informasjonen vises i et diagram der hvert tilgjengelighetstall er en linje som løper langs tidslinjen og beveger seg opp eller ned når antallene endrer seg. Tallene kommer fra den samme motoren som gir informasjon til vinduet **Varetilgjengelighet etter stykklistenivå**. |
|**Stykklistekostandeler – fordeling**|5872|Viser hvordan kostnadene for en montert eller produsert vare er fordelt gjennom stykklisten.<br>Slik informasjon kan være nyttig når du for eksempel skal bestemme om du vil bytte komponentleverandører, erstatte internt kapasitetsforbruk med arbeidskraft som er satt ut, eller omvendt, eller når du gjennomgår og endrer stykklisten for en vare.<br>Det første diagrammet i rapporten viser total enhetskost for den overordnede varens komponenter og arbeidsressurser inndelt i opptil fem ulike kostandeler, presentert grafisk og med ulike farger.<br>Sektordiagrammet som heter *Etter materiale/arbeid*, viser proporsjonal fordeling mellom den overordnede varens materiale og arbeidskostnader, i tillegg til egen indirekte produksjonskost. Materialkostandelen omfatter varens materialkost. Arbeidskostandelen inkluderer kapasitet, indirekte kapasitetskostnader og underleveransekostnader. Kostandelene vises på en annen måte avhengig av valgene i feltet **Vis bare**.<br>Sektordiagrammet som heter *Etter direkte/indirekte*, viser proporsjonal fordeling mellom den overordnede varens direkte og indirekte kostnader. Direkte kostnadsandel omfatter varens materiale, kapasitet og underleveransekostnader. Indirekte kostnadsandel omfatter indirekte kapasitetskostnader og indirekte produksjonskostnader.<br>Tabellen nederst i rapporten er inkludert når du merker av for **Inkluder detaljer**. Den viser valgte verdier fra vinduet Stykklistekostandeler etter enkeltnivå eller opprullert, avhengig av valgene i feltet **Vis kostandeler som**.|
|**Detaljert beregning**|99000756|Viser en kostnadsoversikt per vare som tar vrak med i beregningen.|
|**Inngår i (øverste nivå)**|99000757|Viser hvor i produktstrukturen varene brukes, og hvor de brukes.<br>Rapporten viser bare varen som Inngår i, når basisvaren brukes som vare på øverste nivå. Hvis for eksempel vare A brukes til å produsere vare B, og vare B brukes til å produsere vare C, viser rapporten vare B hvis du kjører denne rapporten for vare A. Hvis du kjører rapporten for vare B, vises vare C som Inngår i.<br>Du kan også åpne siden **Inngår i-linje** direkte fra varen.|
|**Sammenligningsoversikt for varestykkliste**|99000758|Denne rapporten gir deg muligheten til å sammenligne lignende endelige produkter som gjelder kostnadene. Det vises en oversikt over alle komponenter og kostnader i tillegg til de nødvendige antallene. Beregningsdatoen settes vanligvis til arbeidsdatoen. |
|**Produksjonsordrestatistikk**|99000791|Angir de ulike kostbeløpene som er akkumulert for den valgte produksjonsordren.<br>Innholdet i rapporten er veldig lik siden **Produksjonsordrestatistikk**.<br>Når det gjelder produksjonsordrer som bruker produksjonsprinsippet *Produser til ordre*, vises bare material- og kapasitetskostnader for varer på øverste stykklistenivå i vinduet.|
|**Oversikt over kapasitetsoppg.**|99000780|Viser hvilke produksjonsordrer som venter på å bli behandlet ved arbeidssentrene og produksjonsressursene. Utskrifter skrives ut for kapasiteten i arbeidssenteret eller produksjonsressursen. Rapporten tar med opplysninger som start- og sluttidspunkt, dato per produksjonsordre og tilgangsantall.|
|**Arbeidssenterbelastning** eller **Produksjonsressursbelastning**|99000783 eller 99000784|Begge rapportene viser en oversikt over belastningen for et arbeid eller en produksjonsressurs. Belastningen i et arbeid eller en produksjonsressurs er summen av ønsket antall ganger alle planlagte og faktiske ordrer kjøres i arbeidssenteret i en bestemt periode.|
|**Prod.ordre – mankoliste**|99000788|Denne rapporten kan brukes til å vise alle komponenter som ikke er tilgjengelige på grunn av manglende beholdning. Denne oversikten kan for eksempel brukes til å se om tidslinjen for en planlagt eller frigitt produksjonsordre, hvis planlagt tidspunkt kan beholdes.|


## <a name="tasks"></a>Oppgaver

Følgende artikler beskriver noen av de viktige oppgavene for å analysere tilstanden i virksomheten din:

* [Vis belastning på arbeidssentre og produksjonsressurser](production-how-to-view-the-load-on-work-centers.md)  
* [Vis tilgjengeligheten av varer](inventory-how-availability-overview.md)

## <a name="see-also"></a>Se også

[Definere produksjon](production-configure-production-processes.md)  
[Produksjon](production-manage-manufacturing.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
