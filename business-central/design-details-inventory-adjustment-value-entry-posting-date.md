---
title: Bokføringsdato på verdiposter
description: Lær hvordan kjørselen Juster kostverdi - vareposter identifiserer og tilordner en bokføringsdato til verdipostene som kjørselen skal opprette.
author: edupont04
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 07/27/2021
ms.author: edupont
ms.openlocfilehash: 2a3d35672905094e714f85ac4758cbf39ec88cb6
ms.sourcegitcommit: 769d20d299155cba30c35636d02b2ef021e4ecc1
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 07/29/2021
ms.locfileid: "6688317"
---
# <a name="design-details-posting-date-on-adjustment-value-entry"></a>Designdetaljer: Bokføringsdato på verdiposten for justering  

Denne artikkelen gir en beskrivelse av funksjonen for kostberegning av beholdning i [!INCLUDE[prod_short](includes/prod_short.md)]. Denne artikkelen beskriver hvordan kjørselen **Juster kostverdi - vareposter** identifiserer og tilordner en bokføringsdato til verdipostene som kjørselen skal opprette.  

Først gjennomgås begrepet om prosessen, hvordan kjørselen identifiserer og tilordner bokføringsdatoen til verdiposten som skal opprettes. Deretter formidler vi noen scenarier som vi i støtteteamet møter på med jevne mellomrom, og til slutt er det en oppsummering av begrepene.  

## <a name="the-concept"></a>Begrepet  

Kjørselen **Juster kostverdi – vareposter** tilordner en bokføringsdato til verdiposten den skal opprette, på følgende måte:  

1.  Først er bokføringsdatoen for posten som skal opprettes, samme dato som posten den justerer  

2.  Bokføringsdatoen valideres mot lagerperioder og/eller finansoppsett.  

3.  Tilordning av bokføringsdato: Hvis opprinnelig bokføringsdato ikke er innenfor tillatt datointervall for bokføring, tilordner kjørselen en tillatt bokføringsdato fra finansoppsett eller lagerperiode. Hvis både lagerperioder og tillatte bokføringsdatoer i finansoppsett er definert, tilordnes den seneste datoen av de to til verdiposten for justering.  

 La oss se på prosessen ved hjelp av et praktisk eksempel. Anta at vi har en varepost for salg. Varen ble levert 5. september 2020, og den ble fakturert dagen etter.  


**Varepost**  
Datoformat ÅÅÅÅ-MM-DD

|Løpenr.  |Varenr.  |Bokføringsdato  |Posttype  | Bilagsnr. |Lokasjonskode  |Antall  |Kostbeløp (faktisk)  |Fakturert antall  |Restantall  |
|---------|---------|---------|---------|---------|---------|---------|---------|---------|---------|
|319     |A         |2020-09-05     |  Salg       |102033     |  Blå       | -1    |    –11     |-1     |    0     |

Den første verdiposten (379) nedenfor representerer leveringen og har samme bokføringsdato som den overordnede vareposten.  
  
Den andre verdiposten (381) representerer fakturaen.  

Den tredje verdiposten (391) er en justering av faktureringsverdiposten (381).  
  

|Løpenr.  |Varenr.  |Bokføringsdato  |Vareposttype  |Posttype  |Bilagsnr.  |Varepostnr.  |Lokasjonskode  |Varepostantall  |Fakturert antall  |Kostbeløp (faktisk)  |Kostbeløp (forventet)  |Justering  |Utligningspost  |Kildekode  |
|---------|---------|---------|---------|---------|---------|---------|---------|---------|---------|--------|---------|---------|---------|---------|
|379     |  A       |    2020-09-05     |    Salg     | Kjøpspris/prod.kost   | 102033        |319     | Blå        | -1       |0         |  0       |     -10   |Nei   |0    |Salg          |
|381     |  A       |    2020-09-06     |    Salg     | Kjøpspris/prod.kost   | 103022        |319     | Blå        |  0       |-1        |-10       |    10     | Nei  |0      |       Salg   |
|391     |  A       |    2020-09-10     |    Salg     | Kjøpspris/prod.kost   | 103022        |319     | Blå        |  0       |0         |-1        |    0     |Ja   |    181   | LAGERJUST   |

Bokføringsdatoen på justeringsposten angis i førsteomgang til samme bokføringsdato som posten den justerer.

 Trinn 1: Verdiposten for justering som skal opprettes, tildeles samme bokføringsdato som posten den justerer, som vist ovenfor ved verdipost 391.  
  
 Trinn 2: Validering av opprinnelig tilordnet bokføringsdato.  

**Juster kostverdi - vareposter**-kjørselen bestemmer om den første bokføringsdatoen for verdiposten for justering er innenfor tillatt datointervall for bokføring basert på lagerperioder og/eller finansoppsett.  

La oss gå gjennom salget som er angitt ovenfor, ved å legge til oppsett for tillatt bokføringsdatointervall.  
  
**Lagerperioder**

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

Den første tillatte bokføringsdatoen er den første dagen i den første åpne perioden. 1. september 2020.  

**Finansoppsett**

|Felt|Verdi  |
|---------|---------|
|Bokf. tillatt fra:  |  2020-09-10      |
|Bokf. tillatt til:    |  2020-09-30      |
|Registrer tid:       |         |
|Lokalt adresseformat:|   Postnr.      |  

 Første tillatte bokføringsdato er datoen som er angitt i feltet Bokf. tillatt fra: 1. september 2020.  
 Hvis både lagerperioder og tillatte bokføringsdatoer i finansoppsett er definert, definerer den seneste datoen av de to det tillatte bokføringsdatointervallet.  

 Trinn 3: Tilordning av en tillatt bokføringsdato.  

 Første tilordnede bokføringsdato var 6. september, som vist i trinn 1. Men i det andre trinnet identifiserer kjørselen Juster kostverdi – vareposter at den tidligste tillatte bokføringsdatoen er 10. september, og dermed tilordnes 10. september til verdiposten for justeringsposten nedenfor.  

   
|Løpenr.  |Varenr.  |Bokføringsdato  |Vareposttype  |Posttype  |Bilagsnr.  |Varepostnr.  |Lokasjonskode  |Varepostantall  |Fakturert antall  |Kostbeløp (faktisk)  |Kostbeløp (forventet)  |Justering  |Utligningspost  |Kildekode  |
|---------|---------|---------|---------|---------|---------|---------|---------|---------|---------|---------|---------|---------|---------|---------|
|379     |  A       |    2020-09-05     |    Salg     | Kjøpspris/prod.kost   | 102033        |319     | Blå        | -1       |0         |  0       |     -10   |Nei   |0    |Salg          |
|381     |  A       |    2020-09-06     |    Salg     | Kjøpspris/prod.kost   | 103022        |319     | Blå        |  0       |-1        |-10       |    10     | Nei  |0      |       Salg   |
|391     |  A       |    **2020-09-10**     |    Salg     | Kjøpspris/prod.kost   | 103022        |319     | Blå        |  0       |0         |-1        |    0     |Ja   |    181   | LAGERJUST   |

 Vi har nå sett på begrepet om å tilordne bokføringsdatoer til verdiposter som opprettes av kjørselen Juster kostverdi - vareposter.  

 La oss fortsette å se på noen scenarioer som vi i støtteteamet møter på fra tid til annen knyttet til tilordnede bokføringsdatoer i kjørselen Juster kostverdi – vareposter og relaterte oppsett.  

## <a name="scenario-i-posting-date-is-not-within-your-range-of-allowed-posting-dates"></a>Scenario I: Bokføringsdatoen er ikke innenfor tillatte bokføringsdatoer ...  

 Dette er en situasjon der en bruker får denne feilmeldingen når kjørselen Juster kostverdi - vareposter er kjørt.  

 I forrige del der vi beskrev begrepet om tilordning av bokføringsdatoer, var kjørselen Juster kostverdi - vareposter ment å opprette en verdipost med bokføringsdato 10. september.  

![Feilmelding om bokføringsdato.](media/helene/TechArticleAdjustcost6.png "Feilmelding om bokføringsdato")

 Vi følge opp med brukeroppsettet:  

**Brukeroppsett**  

Sortering: bruker-ID  

|Bruker-ID  |Bokf. tillatt fra  | Bokf. tillatt til  |
|---------|---------|--------|
|EUROPA  |  2020-09-11      |2020-09-30      |

 Brukeren i dette tilfellet har et tillatt bokføringstidsrom fra 11. september til 30. september, og kan dermed ikke bokføre justeringsverdiposten med bokføringsdato 10. september.  

### <a name="overview-of-involved-posting-date-setup"></a>Oversikt over involvert oppsett for bokføringsdato:

**Lagerperioder**  

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

**Finansoppsett**  

|Felt|Verdi|
|---------|---------|
|Bokf. tillatt fra:  |  2020-09-10      |
|Bokf. tillatt til:    |  2020-09-30      |
|Registrer tid:       |         |
|Lokalt adresseformat:|   Postnr.      |  

**Brukeroppsett**    

|Bruker-ID  |Bokf. tillatt fra  | Bokf. tillatt til  |
|---------|---------|--------|
|<name> |  2020-09-11      |2020-09-30      |

 Når du tilordner brukeren et bredere (eller samme) tillatte intervall for bokføringsdato som i lagerperioden eller finansoppsettet, blir den nevnte konflikten forhindret. Justeringsverdiposten med bokføringsdato 10. september bokføres med dette oppsettet.

En eldre kunnskapsbaseartikkel [952996](https://support.microsoft.com/topic/information-about-inventory-adjustment-posting-dates-in-microsoft-dynamics-nav-99e22b2b-5b79-a9b2-3b43-7f3484fa31d9) beskriver flere scenarioer knyttet til den nevnte feilmeldingen.  

## <a name="scenario-ii-posting-date-on-adjustment-value-entry-versus-posting-date-on-entry-causing-the-adjustment-such-as-revaluation-or-item-charge"></a>Scenario II: Bokføringsdato på verdipost for justering kontra bokføringsdato på post som forårsaker justeringen, for eksempel revaluering eller varegebyr.  

### <a name="revaluation-scenario"></a>Revalueringsscenario:  

 Forutsetninger:  

 Lageroppsett:  
pf
-   Automatisk kostbokføring = Ja  

-   Automatisk kostjustering = Alltid  

-   Beregn.type for gj.snittskost = vare  

-   Gjennomsnittskostperiode = Dag  

 Finansoppsett:  

-   Bokf. tillatt fra = 1. januar 2021  

-   Bokf. tillatt til = tom  

 Brukeroppsett:  

-   Bokf. tillatt fra = 1. desember 2020  

-   Bokf. tillatt til = tom  

### <a name="to-test-the-scenario"></a>Slik tester du scenarioet  

1.  Opprett varen TEST:  

     Lagerenhet = STK  

     Lagermetode = Gjennomsnitt  

     Velg valgfrie bokføringsgrupper.  

2.  Åpne varekladden, og opprett og bokfør en linje på følgende måte:  

     Bokføringsdato = 15. desember 2020  

     Vare = TEST  

     Posttype = Kjøp  

     Antall = 100  

     Enhetsbeløp = 10  

3.  Åpne varekladden, og opprett og bokfør en linje på følgende måte:  

     Dato = 20. desember 2020  

     Vare = TEST  

     Posttype = Nedjustering  

     Antall = 2  

4.  Åpne varekladden, og opprett og bokfør en linje på følgende måte:  

     Dato = 15. januar 2021  

     Vare = TEST  

     Posttype = Nedjustering  

     Antall = 3  

5.  Åpne revalueringskladden, og opprett og bokfør en linje på følgende måte:  

     Vare = TEST  

     Utligningspost = velg kjøpspost bokført i trinn 2. Bokføringsdatoen for revalueringen blir lik posten den justerer.  

     Enhetskost (revaluert) = 40  

Følgende **vareposter** og **verdiposter** er bokført:  

**Varepost – kjøp**:  
Datoformat ÅÅÅÅ-MM-DD  

|Løpenummer  |Varenr.  |Bokføringsdato  |Posttype  |Bilagsnr.  |Antall  |Kostbeløp (faktisk)  |Restantall  |
|---------|---------|---------|---------|---------|---------|---------|---------|
|317     |TEST         |2020-12-15         |Kjøp         |T00001         |100         |4000         |95        |

**Verdiposter**  

|Løpenummer  |Varenr.  |Bokføringsdato  |Varepostnr.  |Vareposttype  |Posttype  |Bilagsnr.  |Antall varenummerposter  |Kostbeløp (faktisk)  |Bokført kost  |Justering  |Gjelder post  |Kildekode  |
|---------|---------|---------|---------|---------|---------|---------|---------|---------|---------|---------|---------|---------|
|376     |TEST|   2020-12-15    |317         |Kjøp         |Kjøpspris/prod.kost         |T00001         |100         |1 000,00          |1 000,00    |Nei         |0         |VARENP         |
|379     |TEST   |**2020-12-15**    |317         |Kjøp         |Revaluering         |T04002         |0         |3 000,00         |3 000,00         |Nei         |0         |REVALINL         |

**Varepost – nedjustering, trinn 3**  

|Løpenr.  |Varenr.  |Bokføringsdato  |Posttype  |Bilagsnr.  |Antall  |Kostbeløp (faktisk)  |Restantall  |
|---------|---------|---------|---------|---------|---------|---------|---------|
|318     |TEST      |2020-12-20   |Nedjustering  |T00002         |-2         |–80         | 0        |

**Verdiposter**  

|Løpenummer  |Varenr.  |Bokføringsdato  |Varepostnr.  |Vareposttype  |Posttype  |Bilagsnr.  |Antall varenummerposter  |Kostbeløp (faktisk)  |Bokført kost til finans  |Justering  |Gjelder post  |Kildekode  |
|---------|---------|---------|---------|---------|---------|---------|---------|---------|---------|---------|---------|---------|
|377     |TEST|   2020-12-20    |318         |Nedjustering         |Kjøpspris/prod.kost         |T00002         |-2         |–20          |–20    |Nei         |0         |VARENP         |
|380     |TEST   |**2021-01-01**    |318         |Nedjustering         |Kjøpspris/prod.kost         |T04002         |0         |–60         |–60         |Ja         |377         |LAGERJUST         |

**Varepost – nedjustering, trinn 4**  

|Løpenr.  |Varenr.  |Bokføringsdato  |Posttype  |Bilagsnr.  |Antall  |Kostbeløp (faktisk)  |Restantall  |
|---------|---------|---------|---------|---------|---------|---------|---------|
|319     |TEST      |2021-01-15   |Nedjustering  |T00003         |–3         |–120         | 0        |

**Verdiposter**  

|Løpenummer  |Varenr.  |Bokføringsdato  |Varepostnr.  |Vareposttype  |Posttype  |Bilagsnr.  |Antall varenummerposter  |Kostbeløp (faktisk)  |Bokført kost til finans  |Justering  |Gjelder post  |Kildekode  |
|---------|---------|---------|---------|---------|---------|---------|---------|---------|---------|---------|---------|---------|
|378     |TEST|   2021-01-15    |319         |Nedjustering         |Kjøpspris/prod.kost         |T00003         |–3         |-30          |-30    |Nei         |0         |VARENP         |
|381     |TEST   |**2021-01-15**    |319         |Nedjustering         |Kjøpspris/prod.kost         |T04003         |0         |–90         |–90         |Ja         |378         |LAGERJUST         |

Juster kostverdi – vareposter-kjørselen har gjenkjent en endring i kost og justert nedjusteringene.  

**Gjennomgang av bokføringsdatoer på opprettede verdiposter for justering:** Den tidligste tillatte bokføringsdatoen som kjørselen Juster kostverdi - vareposter må relateres til, er 1. januar 2021, som angitt i Finansoppsett.  

**Nedjustering i trinn 3:** Tilordnet bokføringsdato er 1. januar, angitt i finansoppsettet. Bokføringsdatoen for verdiposten i området for justering er 20. desember 2020. I henhold til Finansoppsett er ikke datoen innenfor det tillatte datointervallet for bokføring. Derfor tilordnes bokføringsdatoen som er angitt i feltet Bokf. tillatt fra i finansoppsettet, til verdiposten for justering.  

**Nedjustering i trinn 4:** Tilordnet bokføringsdato er 15. januar. Verdiposten i området for justering har bokføringsdatoen 15. januar, som er innenfor det tillatte bokføringsdatointervallet i henhold til Finansoppsett.  

Justeringen foretatt for nedjusteringen i trinn 3 fører til diskusjon. Den beste bokføringsdatoen for verdiposten for justering ville vært 20. desember eller i det minste i desember siden revalueringen som forårsaker endringen i vareforbruk, ble bokført i desember.  

For å oppnå justering i desember for nedjusteringen i trinn 3, må feltet Bokf. tillatt fra i Finansoppsett angi en dato i desember.  

**Konklusjon:**  

Med erfaringene fra dette scenarioet, når du skal vurdere det best egnede oppsettet for tillatt bokføringsdatointervall for et selskap, kan du vurdere følgende informasjon: Såfremt du tillater endringer i lagerverdien kan bokføres i en periode, desember i dette tilfellet, må oppsettet som selskapet bruker for tillatt bokføringsdatoområde, justeres i henhold til denne beslutningen. Bokf. tillatt fra i finansoppsettet, som angir 1. desember, ville tillatt at revalueringen i desember kunne overføres til påvirkede utgående poster i samme periode.  

Brukergrupper som ikke kan bokføre i desember, men i januar, som sannsynligvis var ment å være begrenset av finansoppsettet i dette scenarioet, bør i stedet løses via brukeroppsettet.  

### <a name="item-charge-scenario"></a>Varegebyrscenario:  

 Forutsetninger:  

 Lageroppsett:  

-   Automatisk kostbokføring = Ja  

-   Automatisk kostjustering = Alltid  

-   Beregn.type for gj.snittskost = vare  

-   Gjennomsnittskostperiode = Dag  

 Finansoppsett:  

-   Bokf. tillatt fra = 1. desember 2020.  

-   Bokf. tillatt til = tom  

 Brukeroppsett:  

-   Bokf. tillatt fra = 1. desember 2020.  

-   Bokf. tillatt til = tom  


### <a name="to-test-the-scenario"></a>Slik tester du scenarioet  

1.  Opprett varegebyr:  

     Lagerenhet = STK  

     Lagermetode = Gjennomsnitt  

     Velg valgfrie bokføringsgrupper.  

2.  Opprett ny bestilling  

     Kjøp fra-leverandørnr.: 10000  

     Bokføringsdato = 15. desember 2020

     Leverandørs fakturanr.: 1234  

     På bestillingslinjen:  

     Vare = GEBYR  

     Antall = 1  

     Direkte enhetskost = 100  

     Bokfør mottak og faktura.  

3.  Opprett ny ordre:  

     Salg til-kundenr.: 10000  

     Bokføringsdato = 16. desember 2020  

     På ordrelinjen:  

     Vare = GEBYR  

     Antall = 1  

     Salgspris = 135  

     Bokfør levering og faktura.  

4.  Finansoppsett:  

     Bokf. tillatt fra = 1. januar 2021  

     Bokf. tillatt til = tom  

5.  Opprett ny bestilling:  

     Kjøp fra-leverandørnr.: 10000  

     Bokføringsdato = 2. januar 2021  

     Leverandørs fakturanr.: 2345  

     På bestillingslinjen:  

     Varegebyr = NC-FRAKT  

     Antall = 1  

     Direkte enhetskost = 3  

     Tilordne varegebyr til kjøpsmottak fra trinn 2.  

     Bokfør mottak og faktura.  


**Status varepost for kjøpstrinn 2**:  
  
|Løpenummer  |Varenr.  |Bokføringsdato  |Posttype  |Bilagsnr.  |Antall  |Kostbeløp (faktisk)  |Restantall  |
|---------|---------|---------|---------|---------|---------|---------|---------|
|324     |GEBYR         |2020-12-15         |Kjøp         |107030         |1         |105         |0        |

**Verdiposter**  

|Løpenummer |Varenr.  |Bokføringsdato  |Varepostnr.  |Vareposttype  |Posttype  |Bilagsnr.  | Varegebyrnr.    |  Varepostantall   |Kostbeløp (faktisk)     |Bokført kost til finans |Justering |Utligningspost |
|---------|---------|---------|---------|---------|---------|---------|---------|---------|---------|---------|---------|---------|
|397      |GEBYR|   2020-12-15    |324         |Kjøp         |Kjøpspris/prod.kost         |108029         |         |1          |100    |100         |NO         |0         |
|399      |GEBYR   |2021-01-02    |324         |Kjøp         |Kjøpspris/prod.kost         |108009         |NCFRAKT         |0         |3         |3         |NO         |0         |


**Status varepostsalg**:  
  
|Løpenr.  |Varenr.  |Bokføringsdato  |Posttype  |Bilagsnr.  |Antall  |Kostbeløp (faktisk)  |Restantall  |
|---------|---------|---------|---------|---------|---------|---------|---------|
|325     |GEBYR         |2020-12-16         |Salg         |102035         |-1         |–105         |0        |

**Verdiposter**  

|Løpenummer |Varenr.  |Bokføringsdato  |Varepostnr.  |Vareposttype  |Posttype  |Bilagsnr.  | Varegebyrnr.    |  Varepostantall   |Kostbeløp (faktisk)     |Bokført kost til finans |Justering |Utligningspost |
|---------|---------|---------|---------|---------|---------|---------|---------|---------|---------|---------|---------|---------|
|398      |GEBYR|   2020-12-16    |325         |Salg         |Kjøpspris/prod.kost         |109024         |         |-1          |-100    |-100         |NO         |0         |
|400      |GEBYR   |2021-01-01    |325         |Salg         |Kjøpspris/prod.kost         |109024         |         |0         |–3         |–3         |Ja         |398         |


6.  På arbeidsdatoen 3. januar kommer en kjøpsfaktura som inneholder et ekstra varegebyr for kjøpet som ble gjort i trinn 2. Denne fakturaen har bilagsdato 30. desember, og bokføres derfor med bokføringsdatoen 30. desember 2020.  

     Opprett ny bestilling:  

     Kjøp fra-leverandørnr.: 10000  

     Bokføringsdato = 30. desember 2020  

     Leverandørs fakturanr.: 3456  

     På bestillingslinjen:  

     Varegebyr = NC-FRAKT  

     Antall = 1  

     Direkte enhetskost = 2  

     Tilordne varegebyr til kjøpsmottak fra trinn 2  

     Bokfør mottak og faktura.  


**Status varepost for kjøp**:  

|Løpenummer  |Varenr.  |Bokføringsdato  |Posttype  |Bilagsnr.  |Antall  |Kostbeløp (faktisk)  |Restantall  |
|---------|---------|---------|---------|---------|---------|---------|---------|
|324     |GEBYR         |2020-12-15         |Kjøp         |107030         |1         |105         |0        |

**Verdiposter**  

|Løpenr. |Varenr.  |Bokføringsdato  |Varepostnr.  |Vareposttype  |Posttype  |Bilagsnr.  | Varegebyrnr.    |  Varepostantall   |Kostbeløp (faktisk)     |Bokført kost til finans |Justering |Utligningspost |
|---------|---------|---------|---------|---------|---------|---------|---------|---------|---------|---------|---------|---------|
|397      |GEBYR   |2020-12-15    |324         |Kjøp         |Kjøpspris/prod.kost         |108029         |            |1         |100    |100         |Nei         |0         |
|399      |GEBYR   |2021-01-02    |324         |Kjøp         |Kjøpspris/prod.kost         |108030         |NCFRAKT   |0         |3         |3         |Nei         |0         |
|401      |GEBYR   |**2020-12-30**    |324         |Kjøp         |Kjøpspris/prod.kost         |108031         |NCFRAKT   |0         |2         |2         |Nei         |0         |

**Status varepostsalg**:  
  
|Løpenummer  |Varenr.  |Bokføringsdato  |Posttype  |Bilagsnr.  |Antall  |Kostbeløp (faktisk)  |Restantall  |
|---------|---------|---------|---------|---------|---------|---------|---------|
|325     |GEBYR         |2020-12-16         |Salg         |102035         |-1         |–105         |0        |

**Verdiposter**  

|Løpenr. |Varenr.  |Bokføringsdato  |Varepostnr.  |Vareposttype  |Posttype  |Bilagsnr.  | Varegebyrnr.    |  Varepostantall   |Kostbeløp (faktisk)     |Bokført kost til finans |Justering |Utligningspost |
|---------|---------|---------|---------|---------|---------|---------|---------|---------|---------|---------|---------|---------|
|398      |GEBYR   |2020-12-16        |325         |Salg         |Kjøpspris/prod.kost         |103024         |            |-1         |-100       |-100         |Nei         |0         |
|400      |GEBYR   |2021-01-01        |325         |Salg         |Kjøpspris/prod.kost         |103024         |            |0          |–3         |–3         |Ja         |398         |
|402      |GEBYR   |**2021-01-01**    |325         |Salg         |Kjøpspris/prod.kost         |103024         |            |0          |-2         |-2         |Ja         |398         |

Lagerverdisettingsrapporten skrives ut per 31. desember 2020

![Innholdet i rapporten Lagerverdisetting.](media/helene/TechArticleAdjustcost13.png "Innholdet i rapporten Lagerverdisetting")

 **Sammendrag av scenarioet:**  

 Det beskrevne scenarioet ender opp med en lagerverdisettingsrapport som viser antall = 0 når verdien = 2. Varegebyret som ble bokført i trinn 11, er del av lagerøkningsverdien i desember, mens lagerreduksjonen i samme periode påvirkes ikke.  

 At Finansoppsett angir Bokf. tillatt fra 1. januar var nyttig for det første varegebyret. Kostnadene ved lagerøkning og -reduksjon ble registrert i samme periode. For det andre varegebyret derimot, fører finansoppsettet til at endringen i vareforbruk føres på perioden etter.  

 **Konklusjon:**  

 Det er utfordrende å få lagerverdisettingsrapporten til å vise antall = 0 når verdien <> 0. I dette tilfellet er det også vanskeligere å uttrykke optimale innstillinger når du har kjøpsfakturaer som kommer på samme dag, men på forskjellige perioder eller regnskapsår. Kryssing til et nytt regnskapsår krever vanligvis noe planlegging, og som en del av innsikten fra Juster kostverdi - vareposter-prosessen må føring av vareforbruk vurderes.  

 I dette scenarioet kunne ett alternativ ha vært å angi en dato i desember for noen flere dager i feltet Bokf. tillatt fra i Finansoppsett, og utsette bokføringen av det første varegebyret, slik at alle kostnader for forrige periode/regnskapsår føres for perioden de tilhører først, og kjøre kjørselen Juster kostverdi - vareposter, og deretter flytte den tillatte bokføringsdatoen til den nye perioden\/regnskapsåret. Det første varegebyret med bokføringsdato 2. januar kunne deretter bli bokført.  

## <a name="history-of-adjust-cost--item-entries-batch-job"></a>Historikk for kjørselen Juster kostverdi - vareposter  

 Nedenfor finner du et sammendrag av begrepet om tilordning av bokføringsdatoer til verdiposter for justering med kjørselen Juster kostverdi – vareposter.  

### <a name="about-the-request-form-posting-date"></a>Om forespørselsskjemaet Bokføringsdato:  

 Det finnes ikke lenger en bokføringsdato som skal angis i forespørselsskjemaet for kjørselen Juster kostverdi - vareposter. Kjørselen kjører gjennom alle nødvendige endringer og oppretter verdiposter med bokføringsdatoen for verdiposten den justerer. Hvis bokføringsdatoen ikke er innenfor tillatt datointervall for bokføring, brukes bokføringsdatoen i feltet Bokf. tillatt fra i finansoppsettet, eller hvis lagerperiodene brukes, brukes den seneste datoen av de to. Se beskrevet begrep ovenfor.  

## <a name="history-of-post-inventory-cost-to-gl-batch-job"></a>Historikk for kjørselen Bokfør lagerkost i Finans  

 Kjørselen Bokfør lagerkost i Finans er nært knyttet til kjørselen Juster kostverdi – vareposter, og er grunnen til at denne kjørselen oppsummeres og formidles her også.  
 
![Faktiske kostnader og forventede kostnader.](media/helene/TechArticleAdjustcost14.png "Faktiske kostnader og forventede kostnader")

### <a name="about-the-posting-date"></a>Om bokføringsdatoen  

 Det finnes ikke lenger en bokføringsdato som skal angis i forespørselsskjemaet for kjørselen Bokfør lagerkost i Finans. Finansposten opprettes med samme bokføringsdato som den relaterte verdiposten. For å fullføre kjørselen må det tillatte bokføringsdatointervallet tillate bokføringsdatoen for den opprettede finansposten. Hvis ikke, må det tillatte bokføringsdatointervallet midlertidig åpnes på nytt ved å endre eller fjerne datoene i feltet Bokf. tillatt fra og Tillat bokf. til i Finansoppsett. For å unngå avstemmingsproblemer må bokføringsdato for finansposten svare til bokføringsdatoen for verdiposten.  

 Kjørselen søker gjennom tabell 5811 - Bokfør verdipost i Finans for å identifisere verdipostene innenfor området for bokføring i Finans. Tabellen tømmes når du har utført kjørselen.

## <a name="see-also"></a>Se også  

[Designdetaljer: Kostberegning for beholdning](design-details-inventory-costing.md)  
[Designdetaljer: Vareutligning](design-details-item-application.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
