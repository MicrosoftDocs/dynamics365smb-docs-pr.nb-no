---
title: Feilmeldingen «Bokføringsdatoen er ikke innenfor tillatte bokføringsdatoer»
description: Rett feilen bak meldingen «Bokføringsdatoen er ikke innenfor tillatt bokføringsdatoer» når du starter kjørselen Juster kostverdi – vareposter.
author: edupont04
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: null
ms.date: 09/17/2021
ms.author: edupont
---

# <a name="error-message-posting-date-is-not-within-your-range-of-allowed-posting-dates"></a>Feilmeldingen «Bokføringsdatoen er ikke innenfor tillatte bokføringsdatoer»

Når du bruker kjørselen **Juster kostverdi – vareposter**, kan du støte på følgende feilmelding:

**Bokføringsdatoen er ikke innenfor området for tillatte bokføringsdatoer**

Denne feilmeldingen angir at brukeren ikke kan bokføre poster for den aktuelle datoen, og dette kan løses ved å endre brukeroppsettet.

## <a name="change-the-user-setup"></a>Endre brukeroppsettet

|Bruker-ID  |Bokf. tillatt fra  | Bokf. tillatt til  |
|---------|---------|--------|
|EUROPA  |  2020-09-11      |2020-09-30      |

Brukeren i dette tilfellet har et tillatt bokføringstidsrom fra 11. september til 30. september, og kan dermed ikke bokføre justeringsverdiposten med bokføringsdato 10. september.  

### <a name="overview-of-involved-posting-date-setup"></a>Oversikt over involvert oppsett for bokføringsdato

#### <a name="inventory-periods"></a>Lagerperioder

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

#### <a name="general-ledger-setup"></a>Finansoppsett

|Felt|Verdi|
|---------|---------|
|Bokf. tillatt fra:  |  2020-09-10      |
|Bokf. tillatt til:    |  2020-09-30      |
|Registrer tid:       |         |
|Lokalt adresseformat:|   Postnr.      |  

#### <a name="user-setup"></a>Brukeroppsett

|Bruker-ID  |Bokf. tillatt fra  | Bokf. tillatt til  |
|---------|---------|--------|
|BRUKERNAVN |  2020-09-10      |2020-09-30      |

Når du tilordner et større intervall for bokføringsdato som i lagerperioden eller finansoppsettet, blir mulig å unngå konflikten som forårsaker feilmeldingen. Justeringsverdiposten med bokføringsdato 10. september bokføres med dette oppsettet.
  
## <a name="see-also"></a>Se også

[Designdetaljer: Bokføringsdato på verdiposten for justering](design-details-inventory-adjustment-value-entry-posting-date.md)  
[Designdetaljer: Kostberegning for beholdning](design-details-inventory-costing.md)  
[Designdetaljer: Vareutligning](design-details-item-application.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
