---
title: Bokføringsdato for justeringsverdipost sammenlignet med kildeposten
description: 'Finn ut mer om scenarioet «Bokføringsdato på verdipost for justering kontra bokføringsdato på post som forårsaker justeringen, for eksempel revaluering eller varegebyr» når du kjører kjørselen Juster kostverdi – vareposter.'
author: edupont04
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: null
ms.date: 09/17/2021
ms.author: edupont
---

# Bokføringsdato for justeringsverdipost sammenlignet med kildeposten

Denne artikkelen sammenligner Bokføringsdato på verdipost for justering med bokføringsdatoen på posten som fører til kjøring av kjørselen Juster kostverdi – vareposter, særlig et revalueringsscenario og et varekostscenario.

Kjørselen **Juster kostverdi – vareposter** behandler dataene, avhengig av scenarioet og konfigurasjonen av [!INCLUDE[prod_short](includes/prod_short.md)]. I dette avsnittet beskriver vi to separate prosesser, og for hver enkelt vi viser hvilke konsekvenser kjørselen Juster kostverdi – vareposter har på dataene.

## Revalueringsscenario

### Forutsetninger  

Skriv inn følgende verdier:

**Lageroppsett**:  

- Automatisk kostbokføring = Ja  

- Automatisk kostjustering = Alltid  

- Beregn.type for gj.snittskost = vare  

- Gjennomsnittskostperiode = Dag  

**Finansoppsett**:  

- Bokf. tillatt fra = 1. januar 2021  

- Bokf. tillatt til = tom  

**Brukeroppsett**:  

- Bokf. tillatt fra = 1. desember 2020  

- Bokf. tillatt til = tom  

### Slik tester du scenarioet

Test dette scenarioet ved å utføre følgende trinn.

1. Opprett en **vare** som kalles TEST med følgende verdier:  

     - Lagerenhet = STK  

     - Lagermetode = Gjennomsnitt  

     - Velg valgfrie bokføringsgrupper.  

2. Åpne en **varekladden**, opprett deretter en ny post, og bokfør en linje på følgende måte:  

     - Bokføringsdato = 15. desember 2020  

     - Vare = TEST  

     - Posttype = Kjøp  

     - Antall = 100  

     - Enhetsbeløp = 10  

3. Åpne en **varekladden**, opprett deretter en ny post, og bokfør en linje på følgende måte:  

     - Dato = 20. desember 2020  

     - Vare = TEST  

     - Posttype = Nedjustering  

     - Antall = 2  

4. Åpne en **varekladden**, opprett deretter en ny post, og bokfør en linje på følgende måte:  

     - Dato = 15. januar 2021  

     - Vare = TEST  

     - Posttype = Nedjustering  

     - Antall = 3  

5. Åpne en **varerevalueringskladd**, opprett deretter en ny post, og bokfør en linje på følgende måte:  

     - Vare = TEST  

     - Utligningspost = velg kjøpspost bokført i trinn 2. Bokføringsdatoen for revalueringen blir lik posten den justerer.  

     - Enhetskost (revaluert) = 40  

Følgende **vareposter** og **verdiposter** er bokført:  

**Varepost – kjøp**:  

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

**Juster kostverdi – vareposter**-kjørselen har gjenkjent en endring i kost og justert nedjusteringene.  

**Gjennomgang av bokføringsdatoer på opprettede verdiposter for justering:** Den tidligste tillatte bokføringsdatoen som kjørselen Juster kostverdi - vareposter må relateres til, er 1. januar 2021, som angitt i Finansoppsett.  

**Nedjustering i trinn 3:** Tilordnet bokføringsdato er 1. januar, angitt i finansoppsettet. Bokføringsdatoen for verdiposten i området for justering er 20. desember 2020. I henhold til Finansoppsett er ikke datoen innenfor det tillatte datointervallet for bokføring. Derfor tilordnes bokføringsdatoen som er angitt i feltet Bokf. tillatt fra i finansoppsettet, til verdiposten for justering.  

**Nedjustering i trinn 4:** Tilordnet bokføringsdato er 15. januar. Verdiposten i området for justering har bokføringsdatoen 15. januar, som er innenfor det tillatte bokføringsdatointervallet i henhold til Finansoppsett.  

Justeringen foretatt for nedjusteringen i trinn 3 fører til diskusjon. Den beste bokføringsdatoen for verdiposten for justering ville vært 20. desember eller i det minste i desember siden revalueringen som forårsaker endringen i vareforbruk, ble bokført i desember.  

For å oppnå justering i desember for nedjusteringen i trinn 3, må feltet Bokf. tillatt fra i Finansoppsett angi en dato i desember.  

### Konklusjon

Med erfaringen som fås i dette scenarioet, når du vurderer det mest egnede oppsettet for et tillatt bokføringsdatoområde for et selskap, må du huske på følgende. Så lenge du tillater at endringer i lagerverdien bokføres i en periode, for eksempel desember i dette tilfellet, skal oppsettet som selskapet bruker på tillatte bokføringsdatoområder, være justert med denne beslutningen. Bokf. tillatt fra i finansoppsettet, som angir 1. desember, ville tillatt at revalueringen i desember kunne overføres til påvirkede utgående poster i samme periode.  

Brukergrupper som ikke kan bokføre i desember, men i januar, som sannsynligvis var ment å være begrenset av finansoppsettet i dette scenarioet, bør i stedet løses via brukeroppsettet.  

## Varegebyrscenario  

### Forutsetninger  

Skriv inn følgende verdier:

**Lageroppsett**:  

- Automatisk kostbokføring = Ja  

- Automatisk kostjustering = Alltid  

- Beregn.type for gj.snittskost = vare  

- Gjennomsnittskostperiode = Dag  

**Finansoppsett**:  

- Bokf. tillatt fra = 1. desember 2020.  

- Bokf. tillatt til = tom  

**Brukeroppsett**:  

- Bokf. tillatt fra = 1. desember 2020.  

- Bokf. tillatt til = tom  

### Slik tester du scenarioet  

Test dette scenarioet ved å utføre følgende trinn:

1.  Opprett et **varegebyr** med følgende verdier:  

     - Lagerenhet = STK  

     - Lagermetode = Gjennomsnitt  

     - Velg valgfrie bokføringsgrupper.  

2.  Opprett en ny **bestilling** med følgende verdier:  

     - Kjøp fra-leverandørnr.: 10000  

     - Bokføringsdato = 15. desember 2020

     - Leverandørs fakturanr.: 1234  

     Velg følgende verdier på bestillingslinjen:  

     - Vare = GEBYR  

     - Antall = 1  

     - Direkte enhetskost = 100  

     Du fullfører trinnet ved å bokføre dokumentet som mottatt og fakturert.  

3.  Opprett en ny **ordren** med følgende verdier:  

     - Salg til-kundenr.: 10000  

     - Bokføringsdato = 16. desember 2020  

     På ordrelinjen:  

     - Vare = GEBYR  

     - Antall = 1  

     - Salgspris = 135  

     Du fullfører trinnet ved å bokføre dokumentet som mottatt og fakturert.  

4.  Angi verdier for siden **Finansoppsett**:  

     - Bokf. tillatt fra = 1. januar 2021  

    -  Bokf. tillatt til = tom  

5.  Opprett en ny **bestilling** med følgende verdier:  

     - Kjøp fra-leverandørnr.: 10000  

     - Bokføringsdato = 2. januar 2021  

     - Leverandørs fakturanr.: 2345  

     På bestillingslinjen:  

     - Varegebyr = NC-FRAKT  

     - Antall = 1  

     - Direkte enhetskost = 3  

     - Tilordne varegebyret til kjøpsmottak fra trinn 2.  

     Du fullfører trinnet ved å bokføre dokumentet som mottatt og fakturert.  


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

     Opprett en ny **bestilling** med følgende verdier:  

     - Kjøp fra-leverandørnr.: 10000  

     - Bokføringsdato = 30. desember 2020  

     - Leverandørs fakturanr.: 3456  

     Velg følgende verdier på bestillingslinjen:  

     - Varegebyr = NC-FRAKT  

     - Antall = 1  

     - Direkte enhetskost = 2  

     Tilordne varegebyret til kjøpsmottak fra trinn 2  

     Du fullfører trinnet ved å bokføre dokumentet som mottatt og fakturert.  


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

Det beskrevne scenarioet ender opp med en lagerverdisettingsrapport som viser antall = 0 når verdien = 2. Varegebyret som ble bokført i trinn 6, er del av lagerøkningsverdien i desember, mens lagerreduksjonen i samme periode påvirkes ikke.  

At Finansoppsett angir Bokf. tillatt fra 1. januar var nyttig for det første varegebyret. Kostnadene ved lagerøkning og -reduksjon ble registrert i samme periode. For det andre varegebyret derimot, fører finansoppsettet til at endringen i vareforbruk føres på perioden etter.  

**Konklusjon:**  

Det er utfordrende å få lagerverdisettingsrapporten til å vise antall = 0 når verdien <> 0. I dette tilfellet er det også vanskeligere å uttrykke optimale innstillinger når du har kjøpsfakturaer som kommer på samme dag, men på forskjellige perioder eller regnskapsår. Kryssing til et nytt regnskapsår krever vanligvis noe planlegging, og som en del av innsikten fra Juster kostverdi - vareposter-prosessen må føring av vareforbruk vurderes.  

I dette scenarioet kunne ett alternativ ha vært å angi en dato i desember for noen flere dager i feltet Bokf. tillatt fra i Finansoppsett, og utsette bokføringen av det første varegebyret, slik at alle kostnader for forrige periode/regnskapsår føres for perioden de tilhører først, og kjøre kjørselen Juster kostverdi - vareposter, og deretter flytte den tillatte bokføringsdatoen til den nye perioden\/regnskapsåret. Det første varegebyret med bokføringsdato 2. januar kunne deretter bli bokført.  

## Se også  

[Designdetaljer: Bokføringsdato på verdiposten for justering](design-details-inventory-adjustment-value-entry-posting-date.md)  
[Designdetaljer: Kostberegning for beholdning](design-details-inventory-costing.md)  
[Designdetaljer: Vareutligning](design-details-item-application.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
