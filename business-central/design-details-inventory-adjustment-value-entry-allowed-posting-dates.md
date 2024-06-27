---
title: Feilmeldingen «Bokføringsdatoen er ikke innenfor tillatte bokføringsdatoer»
description: Rett feilen bak meldingen «Bokføringsdatoen er ikke innenfor tillatt bokføringsdatoer» når du starter kjørselen Juster kostverdi – vareposter.
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bholtorf
ms.topic: conceptual
ms.search.keywords: null
ms.date: 05/24/2024
ms.service: dynamics-365-business-central
---

# Feilmeldingen «Bokføringsdatoen er ikke innenfor tillatte bokføringsdatoer»

Når du bruker kjørselen **Juster kostverdi – vareposter**, kan du støte på følgende feilmelding:

**Bokføringsdatoen er ikke innenfor området for tillatte bokføringsdatoer**

Denne meldingen angir at du ikke kan bokføre oppføringer for datoen du skrev inn. Du kan omgå dette problemet ved å endre brukeroppsettet.

## Endre brukeroppsettet  

|Bruker-ID  |Bokf. tillatt fra  | Bokf. tillatt til  |
|---------|---------|--------|
|EUROPA  |  2020-09-11      |2020-09-30      |

I dette tilfellet kan du publisere i datoperioden fra 11. september til 30. september. Du kan imidlertid ikke bokføre justeringsverdiposten med 10. september som bokføringsdato.  

### Oversikt over oppsettet for bokføringsdato

#### Lagerperioder

|Sluttdato  |Name  |Lukkede  |
|---------|---------|---------|
|2020-01-31     |2020. januar      |  Ja    |
|2020-02-28     |Februar 2020     |  Ja    |
|2020-03-31     |Mars 2020        |  Ja    |
|2020-04-30     |April 2020        |  Ja    |
|2020-05-31     |Mai   2020        |  Ja    |
|2020-06-30     |Juni   2020       |  Ja    |
|2020-07-31     |Juli  2020        |   Ja   |
|2020-08-31     |August   2020     |   Ja   |
|2020-09-30     |September   2020  |         |
|2020-10-31     |Oktober   2020    |         |
|2020-11-30     |November   2020   |         |
|2020-12-31     |Desember   2020   |         |  

#### Finansoppsett

|Felt|Verdi|
|---------|---------|
|Bokf. tillatt fra:  |  2020-09-10      |
|Bokf. tillatt til:    |  2020-09-30      |
|Registrer tid:       |         |
|Lokalt adresseformat:|   Postnr.      |  

#### Brukeroppsett

|Bruker-ID  |Bokf. tillatt fra  | Bokf. tillatt til  |
|---------|---------|--------|
|BRUKERNAVN |  2020-09-10      |2020-09-30      |

Når du tilordner et større intervall, der du tillater bokføring på sidene **Lagerperiode** eller **Finansoppsett**, blir det mulig å unngå konflikten som forårsaker feilmeldingen. Det bredere området lar deg for eksempel bokføre justeringsverdiposten med 10. september som bokføringsdato.
  
## Se også  

[Utformingsdetaljer: Bokføringsdato på justeringsverdipost](design-details-inventory-adjustment-value-entry-posting-date.md)  
[Designdetaljer: Kostberegning for beholdning](design-details-inventory-costing.md)  
[Designdetaljer: Vareutligning](design-details-item-application.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
