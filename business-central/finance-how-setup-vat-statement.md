---
title: Definere en mva-oppgave
description: Dette emnet forklarer hvordan du definerer en mva-oppgavemal og mva-oppgavenavn for å oppfylle krav fra skattemyndighetene.
author: brentholtorf
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 'VAT, posting, tax, value-added tax'
ms.search.form: '317, 318, 320, 474'
ms.date: 06/16/2021
ms.author: bholtorf
---
# Definer mva-oppgavemaler og mva-oppgavenavn

Skattemyndighetene kan endre, og endrer, kravene sine for bokføring av mva. Mva-oppgavemaler og mva-oppgavenavn kan hjelpe deg med å forberede kommende endringer og få en jevn overgang til de nye kravene. Du kan bruke mva-oppgavemalen til å definere forskjellige rapporter når du velger å skrive ut oppgaven. Hver mva-oppgavemal kan ha flere mva-oppgavenavn som i sin tur definerer beregningene, og du kan opprette et nytt mva-oppgavenavn når behovene endres. Ett navn beregner for eksempel mva for inneværende år basert på gjeldende krav, og en annen beregner mva basert på kravene for neste år. Navn er også for eksempel en metode for å beholde historikken over mva-oppgaveformater, slik at du kan gå tilbake og se hvordan du beregnet mva i tidligere år.

## Slik definerer du en mva-oppgave

Mva-oppgaver lar deg beregne mva-oppgjørsbeløpet for en bestemt periode, for eksempel et kvartal.

1. Velg ikonet ![Lyspære som åpner funksjonen Fortell meg.](media/ui-search/search_small.png "Fortell hva du vil gjøre") og angi **Mva-oppgaver** og velg deretter den relaterte koblingen.  
2. Velg **Navn**-feltet, og velg deretter **Ny** på siden **Mva-oppgavenavn**.
3. Fyll ut de obligatoriske feltene. Vanligvis vil du ha en innstilling for hver enkelt kombinasjon av Mva-bokf.gruppe - firma / Mva-bokføringsgruppe - vare. For radnumre er det fornuftig å bruke tilsvarende numre eller koder som i den offisielle mva-oppgaven [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]  

> [!Tip]
> Du kan filtrere informasjonen som oppgaven inneholder, avhengig av hva du valgte i **Type**-feltet. **Kontosammentelling** er nyttig hvis du vil ha mva fra en bestemt konto.
**Mva-postsammentelling** får mva fra konti som er knyttet til det delene i feltene **Gen. Posting Type**, **Mva-bokf.gruppe - firma**, og/eller **Mva-bokføringsgruppe - vare**. **Radsammentelling** lar deg angi en verdi eller hurtigfilterkriterier i feltet **Radsammentelling**. Hvis du vil ha mer informasjon, kan du se [Søke etter, filtrere og sortere data](ui-enter-criteria-filters.md). **Beskrivelse** brukes ofte for å legge til en merknad til utdraget. Du kan for eksempel bruke den som en overskrift når du har brukt radsammentelling.

## Forhåndsvise mva-oppgaven

Når du har definert en mva-oppgave, kan du forhåndsvise den for å sikre at den oppfyller dine behov.
> [!Tip]
> Det anbefales å ha en inndeling i mva-oppgaven ved å bruke **Type** **Mva-postsammentelling**, og en annen inndeling under ved å bruke **Type** **Kontosammentelling** for å avstemme beløpene basert på **Mva-post**-tabellen sammenlignet med beløpet i **Finanskonti**. Du kan også bruke rapporten **Finans – mva-avstemming** til dette formålet.

1. Velg **Forhåndsvisning**.
2. Angi et datofilter for å begrense oppgaven til en bestemt periode. Hvis du vil ha mer informasjon om hvordan du tilpasser siden for å vise datofilteret, kan du se [Søke etter, filtrere og sortere data](ui-enter-criteria-filters.md).
3. Du kan velge ulike alternativer for å angi hvilken type mva-poster som inkluderes i oppgaven.
4. På linjene hvor **Type**-feltet inneholder **Mva-postsammentelling**, kan du se en oversikt over mva-poster ved å velge beløpet i **Kolonnebeløp**-feltet.
5. Du kan bruke tilpasning til å vise flere felt på linjene. Det kan for eksempel være urealisert grunnlagsbeløp og urealisert mva-beløp hvis du bruker urealisert mva.

## Se relatert [Microsoft-opplæring](/training/paths/process-vat-dynamics-365-business-central/)

## Se også

[Definere merverdiavgift (mva)](finance-setup-vat.md)  
[Definere urealisert merverdiavgift](finance-setup-unrealized-vat.md)  
[Rapportere mva til skattemyndighetene](finance-how-report-vat.md)  
[Arbeide med mva på kjøp og salg](finance-work-with-vat.md)  
[Lokal funksjonalitet i Business Central](about-localization.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]
