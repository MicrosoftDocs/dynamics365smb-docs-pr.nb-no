---
title: Oversikt over kontantstrøm
description: Oversikt over kontantstrømmer inn og ut for å hjelpe forutsi penger som skal mottas og utbetales.
author: jill-kotel-andersson
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: cash flow, money flow, expense and income, liquidity, cash receipts minus cash payments
ms.date: 06/08/2021
ms.author: a-jillk
ms.reviewer: edupont
ms.openlocfilehash: 8359d95b36d6c16b179de2fce400c44fd93ec0f1
ms.sourcegitcommit: 0953171d39e1232a7c126142d68cac858234a20e
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 06/09/2021
ms.locfileid: "6216387"
---
# <a name="cash-flow-overview"></a>Oversikt over kontantstrøm

Å forstå kontantstrømmer inn og ut er nøkkelen til en fremgangsrik virksomhet. Du kan bruke kontantstrøm til å enkelt opprette en prognose på kort sikt som forutsier hvordan og når du forventer at penger skal mottas og betales av bedriften din. Det er viktig for deg å vite at bedriften har nok kontanter til å betale kreditorer og utgifter når de forfaller.

## <a name="definition-of-cash-flow"></a>Definisjon av kontantstrøm

Begrepet *kontantstrøm* brukes til å angi innbetalinger minus utbetalinger i en valgt periode. Det er et anslag over hvor mye penger som du forventer vil flyte inn og ut av bedriften, og det inkluderer prognoseberegnede inntekter og utgifter.

## <a name="cash-flow-overview"></a>Oversikt over kontantstrøm

Illustrasjonen nedenfor viser en oversikt over hvordan du kan arbeide med kontantstrøm.

![Oversikt over kontantstrøm](media/finance_cash_flow_overview.png "Oversikt over kontantstrøm")

- Du definerer en kontantstrømprognose.  

- Du får kontantstrømprognosekilder fra følgende områder:  

  - Finans – Informasjon om likvide midler og budsjetterte inntekter og utgifter i selskapet.  
  - Kjøp – informasjon om de gjeldende åpne leverandørkontoer og eventuell prognoseberegnet gjeld fra åpne bestillinger.  
  - Salg – informasjon om de gjeldende åpne kundekontoer og eventuell prognoseberegnet mottak fra åpne ordrer.  
  - Service – informasjon om åpne serviceordrer.  
  - Aktiva – Informasjon om planlagte salg og budsjetterte innkjøp av aktiva.  
  - Manuell inntekter og utgifter – administrere manuell inntekter og utgifter og inkludere dem i kontantstrømprognosen.  
- Du bruker en satsvis jobb til å overføre informasjon fra områdene i finans, salg, kjøp, tjenester og aktiva til kontantstrømforslaget. Deretter registrerer du forslagslinjer for å generere en kontantstrømprognose.  
- Du bruker forskjellige vinduer, rapporter og diagrammer til å analysere og skrive ut en kontantstrømprognose som er relatert til tilgjengelighets- og tidslinjeoversikter.  

## <a name="making-a-cash-flow-forecast"></a>Lage en kontantstrømprognose

Basert på de registrerte forslagslinjene kan du regelmessig lage en kontantstrømprognose. Følgende oppsett brukes ofte for en kontantstrømprognose. Oppsettet har tre deler:

  - Innbetalinger  
  - Kontantutbetalinger  
  - Netto kontantstrøm eller kassebeholdning  

Innbetalinger gir detaljer om inntekter som bedriften mottar.

*kontantmottak totalt* = *fordringer* + *åpne ordrer* + *åpne serviceordrer* + *salg av aktiva* + *manuelle inntekter* + *budsjetterte inntekter*

> [!NOTE]
> Manuelle inntekter kan være leieinntekter, renter fra økonomiske aktiva eller ny privat kapital. Du kan planlegge manuelle inntekter for en tidsperiode og bruke dem i beregningen av kontantstrømprognose.

Kontantutbetalinger gir detaljer om betalinger gjort av bedriften.

*total for kontantutbetalinger* = *beløp* + *åpne bestillinger* + *aktivainvestering* + *manuelle utgifter* + *budsjetterte utgifter*

> [!NOTE]
> Manuelle utgifter kan være lønn, renter på kreditt eller privat forbruk. Du kan planlegge manuelle utgifter for en tidsperiode og bruke dem i beregningen av kontantstrømprognose.

Netto kontantstrøm eller kassebeholdning beregnes som totale kontantmottak minus totale kontantutbetalinger ved slutten av hver periode.

*netto kontantstrøm* = *kontantmottak totalt* – *total for kontantutbetalinger* + *likvide midler*

Prognosen kan deretter brukes som et internt verktøy for administrativ beslutningstaking som hjelper deg med å planlegge fremover og ta viktige strategiske beslutninger om driften av virksomheten.

## <a name="see-also"></a>Se også
[Definere kontantstrømanalyse](finance-setup-cash-flow-analyses.md)  
[Analyser kontantstrøm](finance-analyze-cash-flow.md)

[!INCLUDE[footer-include](includes/footer-banner.md)]
