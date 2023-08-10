---
title: Bokføringsdato på verdiposter
description: Lær hvordan kjørselen Juster kostverdi - vareposter identifiserer og tilordner en bokføringsdato til verdipostene som kjørselen skal opprette.
author: edupont04
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: null
ms.date: 09/17/2021
ms.author: edupont
---
# <a name="design-details-posting-date-on-adjustment-value-entry"></a>Designdetaljer: Bokføringsdato på verdiposten for justering

Denne artikkelen gir veiledning for brukere av lagerkostfunksjonen i [!INCLUDE[prod_short](includes/prod_short.md)], og spesielt om hvordan kjørselen **Juster kostverdi – vareposter** identifiserer og tilordner en bokføringsdato til verdipostene som kjørselen er i ferd med å opprette.

## <a name="how-posting-dates-are-assigned"></a>Slik tilordnes bokføringsdatoer

Kjørselen **Juster kostverdi – vareposter** tilordner en bokføringsdato til verdiposten den skal opprette, på følgende måte:  

1. Først er bokføringsdatoen for posten som skal opprettes, samme dato som posten den justerer  

2. Bokføringsdatoen valideres mot lagerperioder og/eller finansoppsett.  

3. Tilordning av bokføringsdato: Hvis opprinnelig bokføringsdato ikke er innenfor tillatt datointervall for bokføring, tilordner kjørselen en tillatt bokføringsdato fra finansoppsett eller lagerperiode. Hvis både lagerperioder og tillatte bokføringsdatoer i finansoppsett er definert, tilordnes den seneste datoen av de to til verdiposten for justering.  

La oss se på prosessen ved hjelp av et praktisk eksempel. Anta at vi har en varepost for salg. Varen ble levert 5. september 2020, og den ble fakturert dagen etter.  

#### <a name="item-ledger-entry"></a>Varepost

|Løpenr.  |Varenr.  |Bokføringsdato  |Posttype  | Bilagsnr. |Lokasjonskode  |Antall  |Kostbeløp (faktisk)  |Fakturert antall  |Restantall  |
|---------|---------|---------|---------|---------|---------|---------|---------|---------|---------|
|319     |A         |2020-09-05     |  Salg       |102033     |  Blå       | -1    |    –11     |-1     |    0     |

Nedenfor finner du relaterte verdiposter:

- **Løpenr. 379** representerer leveringen og har samme bokføringsdato som den overordnede vareposten.  
- **Løpenr. 381** representerer fakturaen.  
- **Løpenr. 391** er en justering av faktureringsverdiposten (løpenr. 381 ovenfor).  

|Løpenr.  |Varenr.  |Bokføringsdato  |Vareposttype  |Posttype  |Bilagsnr.  |Varepostnr.  |Lokasjonskode  |Varepostantall  |Fakturert antall  |Kostbeløp (faktisk)  |Kostbeløp (forventet)  |Justering  |Utligningspost  |Kildekode  |
|---------|---------|---------|---------|---------|---------|---------|---------|---------|---------|--------|---------|---------|---------|---------|
|379     |  A       |    2020-09-05     |    Salg     | Kjøpspris/prod.kost   | 102033        |319     | Blå        | -1       |0         |  0       |     -10   |Nei   |0    |Salg          |
|381     |  A       |    2020-09-06     |    Salg     | Kjøpspris/prod.kost   | 103022        |319     | Blå        |  0       |-1        |-10       |    10     | Nei  |0      |       Salg   |
|391     |  A       |    2020-09-10     |    Salg     | Kjøpspris/prod.kost   | 103022        |319     | Blå        |  0       |0         |-1        |    0     |Ja   |    181   | LAGERJUST   |

For å tilordne bokføringsdatoen for **løpenr. 391** ble følgende trinn brukt:

1. **Verdiposten for justering** som skal opprettes (**Løpenr. 391**), tildeles samme **bokføringsdato** som posten den justerer.

2. **Juster kostverdi - vareposter**-kjørselen bestemmer om den første bokføringsdatoen for verdiposten for justering er innenfor tillatt datointervall for bokføring basert på lagerperioder og/eller finansoppsett.  

La oss gå gjennom salget som er angitt ovenfor, ved å legge til oppsett for tillatt bokføringsdatointervall.  
  
#### <a name="inventory-periods"></a>Lagerperioder

|Sluttdato  |Name  |Lukkede  |
|---------|---------|---------|
|2020-01-31     |2020. januar      |  Ja    |
|2020-02-28     |Februar 2020     |  Ja    |
|2020-03-31     |Mars 2020        |  Ja    |
|2020-04-30     |April 2020        |  Ja    |
|2020-05-31     |Mai   2020        |  Ja    |
|2020-06-30     |Juni   2020       |  Ja    |
|2020-07-31     |Juli  2020        |  Ja    |
|2020-08-31     |August   2020     |  Ja    |
|2020-09-30     |September   2020  |         |
|2020-10-31     |Oktober   2020    |         |
|2020-11-30     |November   2020   |         |
|2020-12-31     |Desember   2020   |         |

Den første tillatte bokføringsdatoen er den første dagen i den første åpne perioden, som er 1. september 2020.  

#### <a name="general-ledger-setup"></a>Finansoppsett

|Felt|Verdi  |
|---------|---------|
|Bokf. tillatt fra:  |  2020-09-10      |
|Bokf. tillatt til:    |  2020-09-30      |
|Registrer tid:       |         |
|Lokalt adresseformat:|   Postnr.      |  

Den første tillatte bokføringsdato er datoen som er angitt i feltet **Bokf. tillatt fra**: 10. september 2020. Hvis både lagerperioder og tillatte bokføringsdatoer i **finansoppsett** er definert, definerer den seneste datoen av de to det tillatte bokføringsdatointervallet.  

**Tilordning av en tillatt bokføringsdato**  

Første tilordnede bokføringsdato var 6. september, som vist i trinn 1. Men i det andre trinnet identifiserer kjørselen Juster kostverdi – vareposter at den tidligste tillatte bokføringsdatoen er 10. september, og dermed tilordnes 10. september til verdiposten for justeringsposten (**løpenr. 391**) nedenfor.  


|Løpenr.  |Varenr.  |Bokføringsdato  |Vareposttype  |Posttype  |Bilagsnr.  |Varepostnr.  |Lokasjonskode  |Varepostantall  |Fakturert antall  |Kostbeløp (faktisk)  |Kostbeløp (forventet)  |Justering  |Utligningspost  |Kildekode  |
|---------|---------|---------|---------|---------|---------|---------|---------|---------|---------|---------|---------|---------|---------|---------|
|379     |  A       |    2020-09-05     |    Salg     | Kjøpspris/prod.kost   | 102033        |319     | Blå        | -1       |0         |  0       |     -10   |Nei   |0    |Salg          |
|381     |  A       |    2020-09-06     |    Salg     | Kjøpspris/prod.kost   | 103022        |319     | Blå        |  0       |-1        |-10       |    10     | Nei  |0      |       Salg   |
|391     |  A       |    **2020-09-10**     |    Salg     | Kjøpspris/prod.kost   | 103022        |319     | Blå        |  0       |0         |-1        |    0     |Ja   |    181   | LAGERJUST   |

## <a name="common-problems-with-the-adjust-cost---item-entries-batch-job"></a>Vanlige problemer med kjørselen Juster kostverdi – vareposter

Det finnes to scenarioer som kundestøtteteamet ofte støter på, og som er hyppige nok til å få sine egne artikler om problemløsning.

### <a name="error-message-posting-date-is-not-within-your-range-of-allowed-posting-dates"></a>Feilmeldingen «Bokføringsdatoen er ikke innenfor tillatte bokføringsdatoer»

Hvis du får denne feilmeldingen, må du justere datoene brukeren har lov til å bokføre poster for. Hvis du vil finne ut mer, kan du se [Feilmeldingen «Bokføringsdatoen er ikke innenfor tillatte bokføringsdatoer»](design-details-inventory-adjustment-value-entry-allowed-posting-dates.md).

### <a name="posting-date-on-adjustment-value-entry-versus-posting-date-on-entry-causing-the-adjustment-such-as-revaluation-or-item-charge"></a>Bokføringsdato på verdipost for justering kontra bokføringsdato på post som forårsaker justeringen, for eksempel revaluering eller varegebyr

Hvis du vil ha mer informasjon, kan du se [Bokføringsdato for justeringsverdipost sammenlignet med kildeposten](design-details-inventory-adjustment-value-entry-source-entry.md).

## <a name="see-also"></a>Se også

[Designdetaljer: Kostberegning for beholdning](design-details-inventory-costing.md)  
[Designdetaljer: Vareutligning](design-details-item-application.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
